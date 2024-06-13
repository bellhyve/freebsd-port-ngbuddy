PORTNAME=	ngbuddy
DISTVERSIONPREFIX=	v
DISTVERSION=	1.0-rc1
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
	${MKDIR} ${STAGEDIR}${_NGBUDDY_SHARE}
	${INSTALL_DATA} ${WRKSRC}/share/ngbuddy/* ${STAGEDIR}${_NGBUDDY_SHARE}
	${MKDIR} ${STAGEDIR}${_NGBUDDY_SHARE}/examples
	${INSTALL_DATA} ${WRKSRC}/examples/* ${STAGEDIR}${_NGBUDDY_SHARE}/examples/
	${MKDIR} ${STAGEDIR}${PREFIX}/share/man/man8/
	${INSTALL_MAN} ${WRKSRC}/ngbuddy.8 ${STAGEDIR}${PREFIX}/share/man/man8/

.include <bsd.port.mk>
