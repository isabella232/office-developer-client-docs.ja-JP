---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ce34b9b3b3c2f8a3a3f6814507225145eb39d86b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564435"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI メッセージ フラグは、下位互換性を維持するために TNEF フラグにマップされます。 すべてのフラグがグループ化され、1 バイトでエンコードされます。 マッピングは次のとおりです。
  
|**MAPI メッセージ フラグ**|**TNEF フラグ**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
これらのフラグは TNEF で定義されます。H ヘッダー ファイル。
  

