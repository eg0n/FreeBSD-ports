# Created by: ijliao
# $FreeBSD$

PORTNAME=	gambit
PORTVERSION=	14.1.0
CATEGORIES=	math
MASTER_SITES=	SF/${PORTNAME}/${PORTNAME}${PORTVERSION:R:R}/${PORTVERSION}

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Library of tools for doing computation in game theory

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		compiler:c++11-lib
USE_GNOME=	gtk20
USE_WX=		3.0
USE_CXXSTD=	c++11
WX_CONF_ARGS=	absolute
WX_UNICODE=	yes
GNU_CONFIGURE=	yes
USE_LDCONFIG=	yes

post-install:
	${INSTALL_DATA} ${WRKSRC}/gambit.desktop \
		${STAGEDIR}${PREFIX}/share/applications
	${INSTALL_DATA} ${WRKSRC}/src/gui/bitmaps/gambit.xpm \
		${STAGEDIR}${PREFIX}/share/pixmaps

.include <bsd.port.mk>
