---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 43765cddb2f06bfbe58e0a4000c7eadfdc5f3347
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803831"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**適用対象**: Outlook 
  
メッセージのスレッドでメッセージが属していることを示します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a>パラメーター

 _cbParent_
  
> [in]親スレッドのインデックス内のバイト数をカウントします。
    
 _lpbParent_
  
> [in]親スレッドのインデックス内のバイトへのポインター。 _CbParent_が 0 の場合、NULL があります。 
    
 _lpcbIndex_
  
> [out]呼び出しによって返される新しい会話のインデックス内のバイト数へのポインター。 
    
 _lppbIndex_
  
> [out]呼び出しによって返される新しい会話のインデックスへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    

