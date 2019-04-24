---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331914"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**attAttachRenddata**属性は、添付ファイルがメッセージテキスト内でどのようにレンダリングされるかを示す、 **RENDDATA**構造体としてエンコードされます。 **RENDDATA**構造体は、単に TNEF ストリームで、 **RENDDATA**構造の最初のメンバーから始まる**sizeof (RENDDATA)** バイトでエンコードされます。 **RENDDATA**構造体の**dwFlags**メンバーの値が**MAC_BINARY**に設定されている場合、次の添付ファイルのデータは MacBinary 形式で格納されます。それ以外の場合、添付ファイルデータは通常どおりにエンコードされます。
  

