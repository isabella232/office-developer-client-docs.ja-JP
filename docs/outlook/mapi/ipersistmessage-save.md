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
  
変更したフォームを、読み込みまたは作成されたメッセージに保存し直します。
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>パラメーター

 _pmessage_
  
> 順番メッセージへのポインター。
    
 _fsameasload_
  
> 順番_pmessage_が指すメッセージが、フォームが読み込まれた、または作成されたメッセージであることを示す場合は TRUE。それ以外の場合は FALSE。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームが正常に保存されました。
    
## <a name="remarks"></a>解説

フォームビューアーは、 **IPersistMessage:: save**メソッドを呼び出して、変更されたフォームを読み込みまたは作成されたメッセージに戻します。 
  
 **Save**は、フォームが[通常](normal-state.md)の状態にある場合にのみ呼び出す必要があります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

保存された変更をコミットしません。変更をコミットするのは発信者のことです。 [**保存**] 呼び出し時以外は、フォームのメッセージに属するプロパティを変更しないでください。 
  
_fsameasload_が TRUE に設定されている場合は、フォームの既存のメッセージに対する変更を保存できます。 _fsameasload_が FALSE に設定されている場合は、保存を実行する前に、元のメッセージのすべてのプロパティを_pmessage_で示されるメッセージにコピーする必要があります。 元のメッセージの[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを使用して、プロパティをコピーします。 
  
すべてのプロパティがコピーされたら、 [noscribble](noscribble-state.md)状態を入力します。 エラーが発生しない場合は、S_OK を返します。 それ以外の場合は、失敗したアクションからエラーを返します。 
  
フォームが通常以外の状態になっているときに**Save**を呼び出すと、E_UNEXPECTED が返されます。 
  
ストレージオブジェクトの保存の詳細については、 [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)メソッドのドキュメントを参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[フォームの状態](form-states.md)

