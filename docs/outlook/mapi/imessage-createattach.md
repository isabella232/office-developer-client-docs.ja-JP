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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9cc2f5f3880466c0a70febedbc7aaec987b62bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572093"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
  
> [in]メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 パラメーターに NULL が返されるメッセージの標準的なインタ フェース、または**IMessage**、発生します。 
    
 _ulFlags_
  
> [in]添付ファイルを作成する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に戻す、可能性のある添付ファイルが呼び出し側のクライアントに完全にアクセスする前に**CreateAttach**を使用できます。 添付ファイルがアクセスできない場合は、エラーにつながるに後続の呼び出しを行います。 
    
 _lpulAttachmentNum_
  
> [out]新しく作成された添付ファイルを識別するインデックス番号へのポインター。 この番号は、メッセージ、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティの基礎となる場合にのみ有効です。
    
 _lppAttach_
  
> [out]添付ファイルを開くオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 添付ファイルが正常に作成されました。
    
## <a name="remarks"></a>注釈

**IMessage::CreateAttach**メソッドでは、メッセージに新しい添付ファイルを作成します。 新しい添付ファイルと、それに設定されている任意のプロパティは利用可能な添付ファイルの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドとメッセージの**IMAPIProp::SaveChanges**メソッドの両方にクライアントが呼び出されるまで。 
  
_LpulAttachmentNum_で指定された添付ファイル数は、一意であり、メッセージのコンテキスト内でのみ有効です。 2 種類のメッセージで 2 つの添付ファイルは同じメッセージに添付ファイルを 2 つ、同じ番号を持つことができます。 
  
## <a name="see-also"></a>関連項目



[IMessage: IMAPIProp](imessageimapiprop.md)

