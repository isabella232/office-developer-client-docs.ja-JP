---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 22735e5d165fb61043bb6433ba84567bf1b3f957
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567362"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しい添付ファイルを作成します。
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>パラメーター

 _lpInterface_
  
> [in]メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、メッセージの標準インターフェイス **(IMessage)** が返されます。 
    
 _ulFlags_
  
> [in]添付ファイルの作成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> **CreateAttach を** 正常に返す (おそらく、呼び出し元のクライアントが添付ファイルに完全にアクセスできる前に) 許可します。 添付ファイルにアクセスできない場合は、後続の呼び出しでエラーが発生する可能性があります。 
    
 _lpulAttachmentNum_
  
> [out]新しく作成された添付ファイルを識別するインデックス番号へのポインター。 この番号は、メッセージが開いている場合にのみ有効で、添付ファイルのプロパティ **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティPR_ATTACH_NUM基になります。
    
 _lppAttach_
  
> [out]開いている添付ファイル オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 添付ファイルが正常に作成されました。
    
## <a name="remarks"></a>注釈

**IMessage::CreateAttach メソッドは**、メッセージに新しい添付ファイルを作成します。 新しい添付ファイルと設定されているプロパティは、クライアントが添付ファイルの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドとメッセージの **IMAPIProp::SaveChanges** メソッドの両方を呼び出すまで使用できません。 
  
_lpulAttachmentNum_ が指す添付ファイル番号は一意であり、メッセージのコンテキスト内でのみ有効です。 つまり、2 つの異なるメッセージ内の 2 つの添付ファイルは同じ番号を持ち、同じメッセージ内の 2 つの添付ファイルは使用できません。 
  
## <a name="see-also"></a>関連項目



[IMessage: IMAPIProp](imessageimapiprop.md)

