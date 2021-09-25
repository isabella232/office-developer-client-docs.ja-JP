---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9c37bd8613f8dc344fad841309b26fb763639935
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609545"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ スレッド内のメッセージが属する場所を示します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in]親会話インデックスのバイト数。
    
 _lpbParent_
  
> [in]親会話インデックス内のバイトへのポインター。 cbParent が 0 の  _場合は_ NULL になります。 
    
 _lpcbIndex_
  
> [out]呼び出しによって返される新しい会話インデックス内のバイト数へのポインター。 
    
 _lppbIndex_
  
> [out]呼び出しによって返される新しい会話インデックスへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    

