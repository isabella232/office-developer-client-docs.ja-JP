---
title: OLE for MAPI の初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 91552ba5a37915ad8a75bd49038e6e90585bd615
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564100"
---
# <a name="initializing-ole-for-mapi"></a>OLE for MAPI の初期化

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
OLE も使用する場合は、OLE 関数 [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) を呼び出して OLE ライブラリを初期化します。 **OleInitialize は** 、セッションのグローバル データを初期化し、呼び出しを受け入れる OLE ライブラリを準備します。 **OleInitialize の呼び出しの詳細については、SDK** のWindowsしてください。
  

