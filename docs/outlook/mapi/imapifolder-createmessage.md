---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d7e6dfbf9e6a751845adb2319b66462bcde651f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800472"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**適用対象**: Outlook 
  
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
  
> [in]新しいメッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 に対する、IID_IMAPIProp、IID_IMAPIContainer、および IID_IMAPIFolder は、有効なインターフェイス識別子が含まれます。 メッセージ ストア プロバイダーは、標準的なメッセージのインターフェイスを取得すると、NULL を渡す[IMessage: IMAPIProp](imessageimapiprop.md)。 
    
 _ulFlags_
  
> [in]メッセージを作成する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
ITEMPROC_FORCE
  
> 示す個人用フォルダー ストア (PST) の対象となるメッセージがルール ストアが、新しいメッセージの到着をリッスンしているすべてのクライアントに通知する前に処理します。 のみを処理するルールは、Exchange Server がサーバー上のメッセージのルールを処理するため、Microsoft Exchange Server のではないサーバー上に作成される新しいメッセージに適用されます。 したがって、プロバイダーまたはクライアントがメッセージを作成する渡す必要がありますこのフラグの組み合わせを[IMAPIPProp::SaveChanges](imapiprop-savechanges.md)にメッセージを保存する際にサーバーが、Exchange Server ではないことを示す、NON_EMS_XP_SAVE を使用しています。 
    
MAPI_ASSOCIATED 
  
> メッセージを作成するのには、標準的な内容のテーブルの代わりに関連する内容の表に含まれなければなりません。 ユーザーとの対話からは、関連するメッセージが表示されません。
    
MAPI_DEFERRED_ERRORS 
  
> **メッセージ**は、作成操作が完全に完了していない場合でも成功することができます。 これは、新しいメッセージが使用できないことをすぐに呼び出し元にことを意味します。 
    
 _lppMessage_
  
> [out]新しく作成したメッセージへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージが正常に作成されました。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::CreateMessage**メソッドでは、ジェネリック、または関連するコンテンツを含む新しいメッセージを作成し、エントリ id を割り当てます。 エントリの識別子は、メッセージ ストア プロバイダーを表す部分と個々 のメッセージを表す部分で構成されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**メッセージ**またはメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドでは、すべての必要なメッセージ プロパティを設定するかどうかを選択することができます。 成功したセーブセットが発生するまで、これらのプロパティを使用できるようにする必要はありません。 
  
関連の情報を処理する方法の詳細については、 [Folder-Associated 情報のテーブル](folder-associated-information-tables.md)と[テーブルの内容](contents-tables.md)を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ ストア プロバイダーの中にすぐに**メッセージ**が返されるメッセージのエントリ id を許可します。その他のメッセージ ストア プロバイダーは、メッセージが保存されるまで、その可用性を遅延します。 すべてのメッセージ ストア プロバイダーは、メッセージの**IMAPIProp::SaveChanges**メソッドを呼び出してするまで、新しいメッセージのエントリ id を生成するため、できないことがあります**メッセージ**が返されるときに、エントリの識別子にアクセスします。 また、新しいメッセージは含まれません、フォルダーの内容のテーブルでの保存が実行されるまで。 
  
になるだけでなく、現在のメッセージ ・ ストア内で一意であるが、最も可能性の高いすべてのメッセージ ストアを同時に開いている新しいメッセージに割り当てられたエントリの識別子を期待してください。 この規則に例外が 1 つは、[プロファイルのメッセージ ストアに複数のエントリが表示されるときに発生します。 これは、メッセージ ・ ストアを複数回開くと重複するエントリの識別子です。 
  
送信メッセージを作成するには、[送信トレイ] フォルダーの**IMAPIFolder::CreateMessage**メソッドを呼び出します。 
  
メッセージが保存される前に、新しいメッセージを格納するフォルダーを削除した場合、結果は定義されていません。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI では、 **IMAPIFolder::CreateMessage**メソッドを使用して、作成し、新しいメッセージを保存します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

