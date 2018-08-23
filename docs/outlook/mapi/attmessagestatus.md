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
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565747"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI メッセージのフラグは、下位互換性を保持するためにフラグを TNEF にマップされます。 すべてのフラグがグループ化され、1 バイトでエンコードします。 マッピングは次のとおりです。
  
|**MAPI メッセージのフラグ**|**TNEF フラグ**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
TNEF では、これらのフラグが定義されています。H ヘッダー ファイルです。
  

