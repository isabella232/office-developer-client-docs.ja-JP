---
title: OLE for MAPI の初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317228"
---
# <a name="initializing-ole-for-mapi"></a>OLE for MAPI の初期化

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ole も使用する場合は、ole ライブラリを初期化するために、ole 関数[oleinitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)を呼び出します。 **oleinitialize**は、セッションのグローバルデータを初期化し、呼び出しを受け入れるように OLE ライブラリを準備します。 **oleinitialize**の呼び出しについては、Windows SDK を参照してください。
  

