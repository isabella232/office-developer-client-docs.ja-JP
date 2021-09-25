---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 426ca9a33444f6130f8ee4eca62164bc835a032c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551416"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいメッセージを作成します。
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a>パラメーター

 _lpInterface_
  
> [in]新しいメッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 有効なインターフェイス識別子には、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、およびIID_IMAPIFolder。 NULL を渡すと、メッセージ ストア プロバイダーは標準のメッセージ インターフェイス [IMessage : IMAPIProp を返します](imessageimapiprop.md)。 
    
 _ulFlags_
  
> [in]メッセージの作成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
ITEMPROC_FORCE
  
> メッセージが新しいメッセージの到着をリッスンしているクライアントに通知する前に、メッセージがルール処理の対象となるかどうかを個人用フォルダー ストア (PST) に示します。 ルール処理は、Microsoft Exchange Server ではないサーバー上に作成された新しいメッセージにのみ適用されます。Exchange Serverサーバー上のメッセージのルールが処理されます。 したがって、メッセージを作成するプロバイダーまたはクライアントは、NON_EMS_XP_SAVE を使用して[IMAPIPProp::SaveChanges](imapiprop-savechanges.md)を使用してメッセージを保存すると組み合わせてこのフラグを渡す必要があります。これは、サーバーが Exchange Server ではないかどうかを示します。 
    
MAPI_ASSOCIATED 
  
> 作成するメッセージは、標準のコンテンツ テーブルではなく、関連付けられたコンテンツ テーブルに含める必要があります。 関連付けられたメッセージは、ユーザーの操作から非表示になります。
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** は、作成操作が完全に完了していない場合でも成功できます。 これは、新しいメッセージが呼び出し元がすぐに使用できない可能性を意味します。 
    
 _lppMessage_
  
> [out]新しく作成されたメッセージへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージが正常に作成されました。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::CreateMessage** メソッドは、汎用または関連付けられたコンテンツを含む新しいメッセージを作成し、エントリ識別子を割り当てる。 エントリ識別子は、メッセージ ストア プロバイダーを表すパーツと、個々のメッセージを表すパーツで構成されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**CreateMessage** で必要なすべてのメッセージ プロパティを設定するか、メッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドで設定するかどうかを選択できます。 保存が正常に行うまで、これらのプロパティを使用可能にする必要があります。 
  
関連情報を使用する方法の詳細については [、「Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables」を参照してください](contents-tables.md)。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

一部のメッセージ ストア プロバイダーでは **、CreateMessage** が返された直後に新しいメッセージのエントリ識別子を使用できます。他のメッセージ ストア プロバイダーは、メッセージが保存されるまで可用性を遅延します。 メッセージ **の IMAPIProp::SaveChanges** メソッドを呼び出すまで、すべてのメッセージ ストア プロバイダーが新しいメッセージのエントリ識別子を生成する場合はないので **、CreateMessage** が返されたときにエントリ識別子にアクセスできない場合があります。 また、保存が行われるまで、新しいメッセージをフォルダーのコンテンツ テーブルに含めません。 
  
新しいメッセージに割り当てられたエントリ識別子は、現在のメッセージ ストア内だけでなく、同時に開いているすべてのメッセージ ストアで一意である可能性が高い場合があります。 このルールの 1 つの例外は、メッセージ ストアの複数のエントリがプロファイルに表示される場合に発生します。 これにより、メッセージ ストアが複数回開き、エントリ識別子が重複します。 
  
送信メッセージを作成するには、Outbox フォルダーの **IMAPIFolder::CreateMessage メソッドを呼び出** します。 
  
メッセージを保存する前に新しいメッセージを含むフォルダーを削除すると、結果は未定義になります。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI は **IMAPIFolder::CreateMessage** メソッドを使用して、新しいメッセージを作成および保存します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

