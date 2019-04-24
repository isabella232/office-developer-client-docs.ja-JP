---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318215"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI メッセージフラグは、下位互換性を維持するために、TNEF フラグにマップされます。 すべてのフラグがまとめられ、1バイトでエンコードされます。 マッピングは次のとおりです。
  
|**MAPI メッセージフラグ**|**TNEF フラグ**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsread  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsmodified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmssubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmslocal  <br/> |
   
これらのフラグは TNEF で定義されています。H ヘッダーファイル。
  

