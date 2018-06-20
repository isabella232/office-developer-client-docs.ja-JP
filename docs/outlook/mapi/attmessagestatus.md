---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799721"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**適用されます**: Outlook 
  
MAPI メッセージのフラグは、下位互換性を保持するためにフラグを TNEF にマップされます。 すべてのフラグがグループ化され、1 バイトでエンコードします。 マッピングは次のとおりです。
  
|**MAPI メッセージのフラグ**|**TNEF フラグ**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
TNEF では、これらのフラグが定義されています。H ヘッダー ファイルです。
  

