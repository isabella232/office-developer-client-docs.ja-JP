---
title: OLE for MAPI の初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388417"
---
# <a name="initializing-ole-for-mapi"></a>OLE for MAPI の初期化

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
OLE を使用する場合は、OLE ライブラリの初期化には、 [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)の OLE 関数を呼び出します。 **OleInitialize**は、セッションのグローバル データを初期化し、OLE ライブラリ呼び出しを受け入れるための準備を行います。 **OleInitialize**呼び出しの詳細については、Windows SDK を参照してください。
  

