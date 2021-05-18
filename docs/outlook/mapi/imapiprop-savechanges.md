---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316633"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最後の保存操作以降にオブジェクトに加えた変更を永続的に行います。 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in] **IMAPIProp::SaveChanges** メソッドが呼び出された場合にオブジェクトに何が起こるかを制御するフラグのビットマスク。 次のフラグを設定できます。 
    
NON_EMS_XP_SAVE
  
> メッセージがサーバーから配信されていないMicrosoft Exchange Server。 このフラグは [、IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドと ITEMPROC_FORCE フラグを組み合わせて使用して、メッセージが個人用フォルダー ファイル (PST) ストアが受信したリッスン クライアントに通知する前に、メッセージがルール処理の対象となるかどうかを PST ストアに示す必要があります。 このルール処理は、Exchange Server ではないサーバー上で[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を使用して作成された新しいメッセージにのみ適用されます。その場合、Exchange Server はメッセージのルールを既に処理している可能性があります。 
    
FORCE_SAVE 
  
> 変更はオブジェクトに書き込み、オブジェクトに対して行われた以前の変更を上書きし、オブジェクトを閉じるべきです。 操作が成功するには、読み取り/書き込みアクセス許可を設定する必要があります。 **SaveChanges** FORCE_SAVE呼び出しが返された後に、このフラグがMAPI_E_OBJECT_CHANGED。 
    
KEEP_OPEN_READONLY 
  
> 変更はコミットする必要があります。オブジェクトは読み取り用に開いたままにしてください。 追加の変更は行う必要はありません。 
    
KEEP_OPEN_READWRITE 
  
> 変更はコミットする必要があります。オブジェクトは読み取り/書き込みアクセス許可のために開いた状態に保つ必要があります。 このフラグは、通常、オブジェクトが読み取り/書き込みアクセス許可のために最初に開かされたときに設定されます。 オブジェクトに対するそれ以降の変更は許可されます。 
    
MAPI_DEFERRED_ERRORS 
  
> **変更が完全に** コミットされる前に、SaveChanges が正常に返されるのを許可します。 
    
SPAMFILTER_ONSAVE
  
> 保存中のメッセージに対するスパム フィルターを有効にする。 スパムのフィルター処理に関するサポートは、送信者の電子メール アドレスの種類が簡易メール転送プロトコル (SMTP) であり、メッセージが個人用フォルダー ファイル (PST) 向けのストアに保存されている場合にのみ使用することができます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 変更のコミットメントは成功しました。
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges は** 、オブジェクトが設定されている場合は読み取り専用KEEP_OPEN_READONLY開いた状態にしたり、設定されている場合は読み取り/書きKEEP_OPEN_READWRITEできません。 変更はコミットされません。 
    
MAPI_E_OBJECT_CHANGED 
  
> オブジェクトは開いた後に変更されました。
    
MAPI_E_OBJECT_DELETED 
  
> オブジェクトは開いた後に削除されています。
    
## <a name="remarks"></a>注釈

**IMAPIProp::SaveChanges** メソッドは、メッセージ、添付ファイル、アドレス帳コンテナー、メッセージング ユーザー オブジェクトなど、処理のトランザクション モデルをサポートするオブジェクトに対してプロパティの変更を永続的に行います。 フォルダー、メッセージ ストア、プロファイル セクションなど、トランザクションをサポートしないオブジェクトは、直ちに変更を永続的に行います。 **SaveChanges への呼び出しは** 必要ありません。 
  
サービス プロバイダーは、すべてのプロパティが保存されるまでオブジェクトのエントリ識別子を生成する必要はないので、 **オブジェクトの PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティは **、SaveChanges** メソッドが呼び出されるまで使用できない場合があります。 一部のプロバイダーは **、SaveChanges** KEEP_OPEN_READONLYに設定されるまで待機します。 KEEP_OPEN_READONLYは、現在の呼び出しに保存する変更が、オブジェクトに対して行われる最後の変更になります。 
  
一部のメッセージ ストアの実装では、クライアントが **SaveChanges** を使用してメッセージの変更を保存し [、IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドを使用してメッセージ オブジェクトを解放するまで、新しく作成されたメッセージをフォルダーに表示しません。 さらに、一部のオブジェクト実装では **、SaveChanges** が呼び出されるまで、新しく作成されたオブジェクトの PR_ENTRYID プロパティを生成できません。また、一部のオブジェクトは _、ulFlags_ で **KEEP_OPEN_READONLY** セットを使用して **SaveChanges** が呼び出された後にのみ生成できます。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

このフラグを受けKEEP_OPEN_READONLY、オブジェクトのアクセスを読み取り/書き込みとして残すオプションがあります。 ただし、プロバイダーは、オブジェクトフラグが渡された場合、オブジェクトを読み取り専用KEEP_OPEN_READWRITEすることはできません。
  
クライアントは、複数の添付ファイルを複数のメッセージに保存すると、すべての添付ファイルとすべてのメッセージに対して **SaveChanges** メソッドを呼び出します。 多くの場合、クライアントはMAPI_DEFERRED_ERRORSを除き、これらの各呼び出しに対して設定されます。 最後の呼び出しまたは以前の呼び出しでエラーを返す場合があります。 フラグは無視できます。 
  
エラーのKEEP_OPEN_READWRITEまたはKEEP_OPEN_READONLYが一緒に設定されている場合MAPI_DEFERRED_ERRORS、エラー延期要求を無視できます。 _ulFlags_ MAPI_DEFERRED_ERRORS設定されていない場合 **、SaveChanges** 呼び出しで以前に延期されたエラーの 1 つを返す可能性があります。 
  
リモート トランスポート プロバイダーがこのメソッドの機能実装を提供するかどうかはオプションであり、実装の他の設計上の選択肢に依存します。 このメソッドを実装する場合は、ここでのドキュメントに従って実行します。 フォルダー オブジェクトと状態オブジェクトは処理されないので、少なくともリモート トランスポート プロバイダーによる **SaveChanges** の実装では、実際に作業を行わずに S_OK を返す必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

クライアントがメソッドを渡KEEP_OPEN_READONLY [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出し、再び **SaveChanges** を呼び出した場合、同じ実装が失敗する可能性があります。 
  
ユーザーがMAPI_E_NO_ACCESS設定した呼び出しからKEEP_OPEN_READWRITEを受け取った後、オブジェクトに対する読み取り/書き込みアクセス許可を持ち続ける必要があります。 SaveChanges を **再度呼び** 出して、KEEP_OPEN_READONLYフラグを渡したり、フラグを指定KEEP_OPEN_SUFFIX。 
  
プロバイダーがアプリケーション フラグをKEEP_OPEN_READWRITEかどうかは、プロバイダーの実装によって異なります。 
  
**SaveChanges** の後にオブジェクトに対して行う唯一の呼び出しが **IUnknown::Release** かどうかを示すために _、ulFlags_ パラメーターにフラグを設定します。 **SaveChanges のエラーは**、保留中の変更を永続的に行えなかねない状況を示します。 SaveChanges 呼び出しのフラグがない場合は、プロバイダー **によって処理** が異なります。 一部のプロバイダーは、この状態をユーザーと同KEEP_OPEN_READONLY。他のプロバイダーは、このプロバイダーと同じKEEP_OPEN_READWRITE。 それでも他のプロバイダーは **、SaveChanges** 呼び出しでフラグを受信しない場合にオブジェクトをシャットダウンします。 
  
一部のプロパティ (通常は計算されたプロパティ) は **、SaveChanges** を呼び出し、場合によっては Release を呼び出すまで処理 **できません**。
  
添付ファイルを複数のメッセージに保存するなどの一括変更を行う場合は  _、ulFlags_ で MAPI_DEFERRED_ERRORSフラグを設定してエラー処理を延期します。 複数の添付ファイルを複数のメッセージに保存する場合は、各添付ファイルに対して **1 つの SaveChanges** 呼び出しを行い、各メッセージに対して **1 つの SaveChanges** 呼び出しを行います。 添付ファイル呼びMAPI_DEFERRED_ERRORS最後のメッセージを除くすべてのメッセージに対して、このフラグを設定します。 
  
**SaveChanges が** オブジェクトをMAPI_E_OBJECT_CHANGED場合は、元のオブジェクトが変更されているかどうかを確認します。 その場合は、変更が以前の変更を上書きするか、オブジェクトを別の場所に保存するかどうかを要求できるユーザーに警告します。 元のオブジェクトが削除されている場合は、別の場所にオブジェクトを保存する機会を与えるユーザーに警告します。 
  
削除された開いているオブジェクトの FORCE_SAVEフラグを使用して **SaveChanges** を呼び出す必要があります。 
  
**SaveChanges が** エラーを返す場合、変更を保存するオブジェクトは _、ulFlags_ パラメーターで設定されたフラグに関係なく開いたままです。 
  
> [!IMPORTANT]
> _ulFlags_ NON_EMS_XP_SAVE および SPAMFILTER_ONSAVE は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加>`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
詳細については、「MAPI プロパティの [保存」を参照してください](saving-mapi-properties.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI プロパティの保存](saving-mapi-properties.md)

