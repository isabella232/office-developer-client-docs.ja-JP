---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351115"
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

 _lpinterface_
  
> 順番メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL 結果をメッセージの標準インターフェイスまたは**IMessage**に渡すと、返されます。 
    
 _ulFlags_
  
> 順番添付ファイルの作成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 添付ファイルが呼び出し元クライアントに完全にアクセス可能になる前に、 **createattach**が正常に戻ることができるようにします。 添付ファイルにアクセスできない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。 
    
 _lアウト attachmentnum_
  
> 読み上げ新しく作成された添付ファイルを識別するインデックス番号へのポインター。 この番号は、メッセージが開いていて、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティの基になっている場合にのみ有効です。
    
 _lppattach_
  
> 読み上げ開かれた attachment オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 添付ファイルが正常に作成されました。
    
## <a name="remarks"></a>解説

**IMessage:: createattach**メソッドは、メッセージに新しい添付ファイルを作成します。 新しい添付ファイルと、そのオブジェクトに設定されているすべてのプロパティは、クライアントが添付ファイルの[imapiprop:: savechanges](imapiprop-savechanges.md)メソッドと、メッセージの**imapiprop:: savechanges**メソッドの両方を呼び出すまでは使用できません。 
  
_lアウト attachmentnum_が指す添付ファイルの番号は一意で、メッセージのコンテキスト内でのみ有効です。 つまり、同じメッセージ内の2つの添付ファイルでは、2つの異なるメッセージの2つの添付ファイルを同じ数にすることができます。 
  
## <a name="see-also"></a>関連項目



[IMessage: IMAPIProp](imessageimapiprop.md)

