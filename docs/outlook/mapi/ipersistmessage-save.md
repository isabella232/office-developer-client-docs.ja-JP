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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397157"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
変更後のフォームを元に読み込みまたは作成したメッセージに保存します。
  
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
  
> [in]メッセージに示されることを指定する場合は TRUE _pMessage_では、メッセージ フォームが読み込まれるか作成。それ以外の場合、FALSE です。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームが正常に保存されました。
    
## <a name="remarks"></a>備考

フォームの閲覧者は、変更後のフォームを元に読み込みまたは作成したメッセージに保存するのには**IPersistMessage::Save**メソッドを呼び出します。 
  
 **保存**する必要がありますのみ呼び出すことは、フォームの[標準](normal-state.md)の状態で。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

保存した変更をコミットしません。変更をコミットする呼び出し元の責任です。 **保存**の呼び出し時に除いて、フォームのメッセージに属するプロパティに変更を加えることはありません。 
  
_FSameAsLoad_が TRUE に設定されている場合は、フォームの既存のメッセージに変更を保存することができます。 _FSameAsLoad_が FALSE に設定されている場合が指す_pMessage_保存を実行する前にメッセージに元のメッセージからコピーすべてのプロパティ必要があります。 プロパティをコピーするのにには、元のメッセージの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを使用します。 
  
すべてのプロパティがコピーされたら、 [NoScribble](noscribble-state.md)の状態を入力します。 エラーが発生しない場合は、S_OK を返します。 それ以外の場合、失敗した操作からのエラーを返します。 
  
フォームは、標準以外の任意の状態にすると、 **Save**が呼び出される、E_UNEXPECTED を返します。 
  
ストレージ ・ オブジェクトを保存する方法の詳細については、[すること](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)の方法のマニュアルを参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[フォームの状態](form-states.md)

