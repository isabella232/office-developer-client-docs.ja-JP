---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309619"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
変更されたフォームを、読み込まれたメッセージまたは作成されたメッセージに保存します。
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>パラメーター

 _pMessage_
  
> [in]メッセージへのポインター。
    
 _fSameAsLoad_
  
> [in]TRUE を指定すると  _、pMessage_ が示すメッセージが、フォームの読み込みまたは作成のメッセージになります。それ以外の場合は FALSE。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームが正常に保存されました。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **、IPersistMessage::Save** メソッドを呼び出して、変更されたフォームを読み込まれたメッセージまたは作成されたメッセージに戻します。 
  
 **保存** は、フォームが標準状態の場合にのみ [呼び出す必要](normal-state.md) があります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

保存された変更をコミットしない。変更をコミットするには、呼び出し元が行います。 Save 呼び出し中を除き、フォームのメッセージに属するプロパティを **変更** しない。 
  
_fSameAsLoad が_ TRUE に設定されている場合は、フォームの既存のメッセージに対する変更を保存できます。 _fSameAsLoad_ が FALSE に設定されている場合は、保存を実行する前に、元のメッセージのすべてのプロパティを _pMessage_ が指すメッセージにコピーする必要があります。 元のメッセージの [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを使用してプロパティをコピーします。 
  
すべてのプロパティがコピーされた場合は [、NoScribble 状態を入力](noscribble-state.md) します。 エラーが発生しない場合は、S_OK。 それ以外の場合は、失敗したアクションからエラーを返します。 
  
フォーム **が Normal** 以外の状態にあるときに Save が呼び出された場合は、次のE_UNEXPECTED。 
  
ストレージ オブジェクトの保存の詳細については [、IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) メソッドのドキュメントを参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[フォームの状態](form-states.md)

