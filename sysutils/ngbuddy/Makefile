PORTNAME=	ngbuddy
DISTVERSIONPREFIX=	v
DISTVERSION=	1.0-rc1
DISTVERSIONPREFIX=	v
CATEGORIES=	sysutils

MAINTAINER=	daniel@belltech.it
COMMENT=	Netgraph Buddy
WWW=		https://github.com/bellhyve/netgraph-buddy

LICENSE=	BSD2CLAUSE

USE_GITHUB=	yes
GH_ACCOUNT=	bellhyve

NO_ARCH=	yes
NO_BUILD=	yes

SUB_FILES=	pkg-message

_NGBUDDY_SHARE=	${PREFIX}/share/ngbuddy

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/ngbuddy ${STAGEDIR}${PREFIX}/etc/rc.d/
	${MKDIR} ${STAGEDIR}${_ZELTA_SHARE}
	${INSTALL_DATA} ${WRKSRC}/share/ngbuddy/* ${STAGEDIR}${_ZELTA_SHARE}
	${MKDIR} ${STAGEDIR}${_ZELTA_SHARE}/examples
	${INSTALL_DATA} ${WRKSRC}/examples/* ${STAGEDIR}${_ZELTA_SHARE}/examples/

.include <bsd.port.mk>
