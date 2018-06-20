---
title: MAPI の OLE の初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6efe41c79cd85eb844ee19b8c54e200956c9b2a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801057"
---
# <a name="initializing-ole-for-mapi"></a>MAPI の OLE の初期化

  
  
**適用されます**: Outlook 
  
OLE を使用する場合は、OLE ライブラリの初期化には、 [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx)の OLE 関数を呼び出します。 **OleInitialize**は、セッションのグローバル データを初期化し、OLE ライブラリ呼び出しを受け入れるための準備を行います。 **OleInitialize**呼び出しの詳細については、Windows SDK を参照してください。
  

