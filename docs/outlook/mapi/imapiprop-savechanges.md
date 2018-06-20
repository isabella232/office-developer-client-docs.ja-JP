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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0a60b813a52779b28124ab6d69b493def35b14aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800671"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**適用されます**: Outlook 
  
前回の保存操作以降は、オブジェクトに対して行われた変更を永続的になります。 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]**IMAPIProp::SaveChanges**メソッドが呼び出されたときにオブジェクトの動作を制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
NON_EMS_XP_SAVE
  
> Microsoft Exchange Server のメッセージが配信されていないことを示します。 このフラグは、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを使用して組み合わせて使用する必要があり、ITEMPROC_FORCE を示すフラグを PST ストア、メッセージの対象とするルールの処理のいずれかの個人用フォルダー ファイル (PST) のストアに通知する前に到着したメッセージをリッスンしているクライアント。 このルールの処理で作成される[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)である場合、Exchange Server ではないサーバーで Exchange Server の新しいメッセージにのみ適用されますが既に処理が、メッセージのルール。 
    
FORCE_SAVE 
  
> オブジェクトに加えられた直前の変更をオーバーライドする、オブジェクトに変更を書き込むし、オブジェクトを閉じる必要があります。 操作を完了するのには、読み取り/書き込みアクセス許可を設定しなければなりません。 **Savechanges メソッド**の呼び出し前に、MAPI_E_OBJECT_CHANGED が返された後は、FORCE_SAVE フラグを使用します。 
    
KEEP_OPEN_READONLY 
  
> 変更をコミットする必要があり、オブジェクトは読み込み用にオープンして保持する必要があります。 追加の変更は行われません。 
    
KEEP_OPEN_READWRITE 
  
> 変更をコミットする必要があり、オブジェクトは、読み取り/書き込みアクセス許可も開いたまま必要があります。 このフラグは通常、読み取り/書き込みのアクセス許可オブジェクトを最初に開いたときに設定されます。 オブジェクトへのそれ以降の変更が許可されています。 
    
MAPI_DEFERRED_ERRORS 
  
> 正常に完了が完全にコミットされた変更前に、 **SaveChanges**を使用できます。 
    
SPAMFILTER_ONSAVE
  
> フィルターが保存されているメッセージに迷惑メールを有効に スパムのフィルタ リングのサポートは、送信者の電子メール アドレスの種類は、簡易メール転送プロトコル (SMTP)、メッセージは個人用フォルダー ファイル (PST) のストアに保存されている場合にのみ使用できます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 変更のコミットに成功しました。
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges**できないオブジェクトを開いたまま読み取り専用のアクセス許可の場合は KEEP_OPEN_READONLY セット、または読み取り/書き込み権限 KEEP_OPEN_READWRITE が設定されている場合。 変更のコミットはありません。 
    
MAPI_E_OBJECT_CHANGED 
  
> オブジェクトは、開かれた後に変更されました。
    
MAPI_E_OBJECT_DELETED 
  
> 開かれた後、オブジェクトが削除されました。
    
## <a name="remarks"></a>備考

**IMAPIProp::SaveChanges**メソッドでは、プロパティの変更を永続的に処理する場合、メッセージ、添付ファイル、アドレス帳コンテナー、およびメッセージングのユーザー オブジェクトのトランザクション モデルをサポートするオブジェクトになります。 フォルダー、メッセージ ストア、およびプロファイルのセクションなどのトランザクションをサポートしないオブジェクト変更永続的なすぐにします。 **Savechanges メソッド**の呼び出しは必要ありません。 
  
サービス プロバイダーは、すべてのプロパティが保存されるまで、そのオブジェクトのエントリ id を生成する必要はありません、ためオブジェクトの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) できない可能性がありますまで、 **SaveChanges**メソッドの後呼び出されました。 プロバイダーによって、KEEP_OPEN_READONLY フラグが設定されるまでの待機、 **SaveChanges**の呼び出しです。 KEEP_OPEN_READONLY は、現在の呼び出しで保存する変更がオブジェクトに対して実行される最後の変更になることを示します。 
  
メッセージ ストアの実装によって操作を行いますフォルダー内のメッセージは新しく作成された表示しないクライアントまで保存して、メッセージ**SaveChanges**を使用して変更[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)メソッドを使用して、メッセージ オブジェクトを解放します。 さらに、いくつかのオブジェクトの実装を生成できません**PR_ENTRYID**プロパティまでの新しく作成されたオブジェクトの後、 **SaveChanges**が呼び出されると、およびいくつかは、KEEP_OPEN_READONLY を使用して、 **SaveChanges**が呼び出された後にのみ_ulFlags_で設定します。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

KEEP_OPEN_READONLY フラグを受信した場合は、オブジェクトの読み取り/書き込みアクセス権をそのままのオプションがあります。 ただし、プロバイダーできますしない状態のままにオブジェクト読み取り専用 KEEP_OPEN_READWRITE フラグが渡される。
  
クライアントは、複数のメッセージに複数の添付ファイルを保存するときに、すべての添付ファイルとすべてのメッセージの**SaveChanges**メソッドを呼び出します。 クライアントでは多くの場合は最後の 1 つを除いて、これらの呼び出しごとに MAPI_DEFERRED_ERRORS を設定します。 最後の呼び出しまたはそれ以前の呼び出しのいずれかのエラーを返すことができます。 フラグを無視してもかまいません。 
  
MAPI_DEFERRED_ERRORS と KEEP_OPEN_READWRITE または KEEP_OPEN_READONLY のいずれかが設定されている場合は、繰延の要求のエラーを無視できます。 延期されていたエラーのいずれかが返されることができます_ulFlags_で MAPI_DEFERRED_ERRORS が設定されていない場合、 **SaveChanges**の呼び出しをします。 
  
リモート トランスポート プロバイダーがこのメソッドの実装の機能を提供するかどうかはオプションであり、他の実装では、設計上の選択によって異なります。 このメソッドを実装する場合は、次のマニュアルに従って。 フォルダー オブジェクトおよびオブジェクトの状態は処理されないため、少なくとも**SaveChanges**のリモート トランスポート プロバイダーの実装する必要があります S_OK を返します実際に作業を行うことがなく。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

KEEP_OPEN_READONLY を渡す、 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すし、 **SaveChanges**を再度呼び出すクライアントに、同じ実装が失敗する可能性があります。 
  
呼び出しから MAPI_E_NO_ACCESS を受信した後を設定すると KEEP_OPEN_READWRITE で引き続きオブジェクトへの読み取り/書き込み権限があります。 **SaveChanges** KEEP_OPEN_READONLY フラグまたは KEEP_OPEN_SUFFIX を持つフラグなしのいずれかを渡すことを呼び出すことができます。 
  
プロバイダーが、KEEP_OPEN_READWRITE フラグをサポートしているかどうかは、プロバイダーの実装によって異なります。 
  
**SaveChanges**の後にオブジェクトに対して実行するだけの呼び出し**が**であることを示す、フラグを設定しない_ulFlags_パラメーターにします。 **SaveChanges**のエラーは、それを作成できませんでした、保留中の変更永続的なことを示します。 別のプロバイダーでは、異なる方法で**SaveChanges**の呼び出しにフラグがない場合を処理します。 プロバイダーによってこの状態と同様に処理 KEEP_OPEN_READONLY です。他のプロバイダーの解釈に KEEP_OPEN_READWRITE と同じです。 まだ他のプロバイダー、 **SaveChanges**の呼び出しフラグを受信しない場合、オブジェクトをシャット ダウンします。 
  
**SaveChanges**が呼び出されるまでと、場合によっては、**リリース**で、通常の計算されたプロパティは、いくつかのプロパティを処理できません。
  
複数のメッセージに添付ファイルを保存するなどの一括変更を加える場合は、 _ulFlags_で MAPI_DEFERRED_ERRORS フラグを設定することで処理中にエラーを延期します。 複数のメッセージに複数の添付ファイルを保存する場合は、1 つ**SaveChanges**の呼び出しの各添付ファイルと 1 つ**SaveChanges**の呼び出しの各メッセージを確認します。 最後の 1 つを除くすべてのメッセージの添付ファイルの呼び出しごとに MAPI_DEFERRED_ERRORS フラグを設定します。 
  
**SaveChanges** MAPI_E_OBJECT_CHANGED が返された場合は、元のオブジェクトが変更されたかどうかを確認します。 その場合は、変更が前の変更を上書きするか、オブジェクトを別の場所での保存を要求できるか、ユーザーと、ユーザーに警告します。 元のオブジェクトが削除されている場合は、別の場所にオブジェクトを保存する機会を与えるユーザーを警告します。 
  
FORCE_SAVE のフラグが削除されているオブジェクトを開くには、 **SaveChanges**を呼び出すことはできません。 
  
**SaveChanges**がエラーを返した場合、オブジェクトの変更をしたまま保存開くには、 _ulFlags_パラメーターで設定されているフラグに関係なく。 
  
> [!IMPORTANT]
> _UlFlags_ダウンロード可能なヘッダー ファイルに現在ある NON_EMS_XP_SAVE および SPAMFILTER_ONSAVE を定義する可能性がない、場合に追加できます、次の値を使用してコード: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
詳細については、 [MAPI プロパティの保存](saving-mapi-properties.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[PidTagEntryId の標準的なプロパティ](pidtagentryid-canonical-property.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MAPI プロパティの保存](saving-mapi-properties.md)

