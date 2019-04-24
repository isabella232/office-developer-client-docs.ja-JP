---
title: imapipropsavechanges
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
  
前回の保存操作以降にオブジェクトに加えられたすべての変更を永続的に行います。 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番**imapiprop:: SaveChanges**メソッドが呼び出されたときに、オブジェクトに対して行われる処理を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
NON_EMS_XP_SAVE
  
> メッセージが Microsoft Exchange サーバーから配信されていないことを示します。 このフラグを[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドおよび ITEMPROC_FORCE フラグと組み合わせて使用して、個人用フォルダーファイル (pst) ストアが通知する前に、ルール処理の対象となるメッセージを pst ストアに示すように指定します。受信したクライアントメッセージが到着したこと。 このルールの処理は、exchange サーバー以外のサーバー上で[imapifolder:: CreateMessage](imapifolder-createmessage.md)を使用して作成された新しいメッセージにのみ適用されます。この場合、exchange サーバーはメッセージに対して既にルールを処理しています。 
    
FORCE_SAVE 
  
> オブジェクトに変更を加えて、オブジェクトに対する以前の変更を上書きし、オブジェクトを閉じる必要があります。 操作を正常に行うには、読み取り/書き込みアクセス許可が設定されている必要があります。 FORCE_SAVE フラグは、以前に**SaveChanges**が MAPI_E_OBJECT_CHANGED を呼び出した後に使用されます。 
    
KEEP_OPEN_READONLY 
  
> 変更を確定して、オブジェクトを読み取り用に開いたままにしておく必要があります。 追加の変更は行われません。 
    
KEEP_OPEN_READWRITE 
  
> 変更をコミットし、オブジェクトを読み取り/書き込みアクセス許可のために開いたままにしておく必要があります。 通常、このフラグは、オブジェクトが読み取り/書き込みアクセス許可で最初に開かれたときに設定されます。 その後、オブジェクトに対する変更を行うことができます。 
    
MAPI_DEFERRED_ERRORS 
  
> 変更が完全にコミットされる前に、 **SaveChanges**が正常に戻ることができるようにします。 
    
SPAMFILTER_ONSAVE
  
> 保存されているメッセージに対してスパムフィルター処理を有効にします。 スパムのフィルター処理に関するサポートは、送信者の電子メール アドレスの種類が簡易メール転送プロトコル (SMTP) であり、メッセージが個人用フォルダー ファイル (PST) 向けのストアに保存されている場合にのみ使用することができます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 変更のコミットメントに成功しました。
    
MAPI_E_NO_ACCESS 
  
> KEEP_OPEN_READONLY が設定されている場合は読み取り専用アクセス許可、KEEP_OPEN_READWRITE が設定されている場合は読み取り/書き込みアクセス許可の場合、 **SaveChanges**ではオブジェクトを開いたままにすることはできません。 変更はコミットされません。 
    
MAPI_E_OBJECT_CHANGED 
  
> オブジェクトが開かれた後に変更されました。
    
MAPI_E_OBJECT_DELETED 
  
> オブジェクトが開かれた後に削除されています。
    
## <a name="remarks"></a>解説

**imapiprop:: SaveChanges**メソッドを使用すると、メッセージ、添付ファイル、アドレス帳コンテナー、メッセージングユーザーオブジェクトなど、処理のトランザクションモデルをサポートするオブジェクトのプロパティの変更を永続的に行うことができます。 フォルダー、メッセージストア、プロファイルセクションなど、トランザクションをサポートしていないオブジェクトは、直ちに変更を反映します。 **SaveChanges**を呼び出す必要はありません。 
  
すべてのプロパティが保存されるまでは、サービスプロバイダーはオブジェクトのエントリ識別子を生成する必要がないため、 **SaveChanges**メソッドの後までオブジェクトの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを使用できない場合があります。が呼び出されました。 一部のプロバイダーは、 **SaveChanges**呼び出しで KEEP_OPEN_READONLY フラグが設定されるまで待機します。 KEEP_OPEN_READONLY は、現在の呼び出しに保存される変更が、オブジェクトに対して最後に行われた変更であることを示します。 
  
メッセージストアの実装によっては、クライアントが**SaveChanges**を使用してメッセージの変更を保存し、 [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを使用してメッセージオブジェクトを解放するまで、新しく作成されたメッセージがフォルダーに表示されないことがあります。 また、一部のオブジェクト実装では、 **savechanges**が呼び出されるまで、新しく作成されたオブジェクトの**PR_ENTRYID**プロパティを生成できません。また、KEEP_OPEN_READONLY を使用して**savechanges**が呼び出された後にのみ実行できるものもあります。_ulflags_で設定します。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

KEEP_OPEN_READONLY フラグを受信した場合は、オブジェクトのアクセスを読み取り/書き込み可能にするオプションがあります。 ただし、KEEP_OPEN_READWRITE フラグが渡された場合、プロバイダーはオブジェクトを読み取り専用状態にしておくことはできません。
  
クライアントが複数のメッセージに複数の添付ファイルを保存すると、すべての添付ファイルとすべてのメッセージに対して**SaveChanges**メソッドが呼び出されます。 多くの場合、クライアントは、これらの呼び出しごとに MAPI_DEFERRED_ERRORS を設定します (最後の呼び出しを除く)。 前回の通話または以前の呼び出しでエラーを返すことができます。 フラグは無視してもかまいません。 
  
KEEP_OPEN_READWRITE または KEEP_OPEN_READONLY のどちらかが MAPI_DEFERRED_ERRORS と共に設定されている場合は、エラー繰延要求を無視できます。 _ulflags_に MAPI_DEFERRED_ERRORS が設定されていない場合は、以前に遅延したエラーの1つを**SaveChanges**呼び出しに対して返すことができます。 
  
リモートトランスポートプロバイダーがこのメソッドの機能実装を提供するかどうかはオプションであり、実装での他の設計上の選択によって異なります。 このメソッドを実装する場合は、ここに記載されているドキュメントに従ってください。 folder オブジェクトと status オブジェクトは処理されないため、少なくともリモートトランスポートプロバイダーの**SaveChanges**の実装は、実際には何も作業を行わずに S_OK を返す必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

クライアントが KEEP_OPEN_READONLY に合格した場合は、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出してから、再度**SaveChanges**を呼び出すと、同じ実装が失敗する可能性があります。 
  
KEEP_OPEN_READWRITE を設定した呼び出しから MAPI_E_NO_ACCESS を受信した後、そのオブジェクトに対する読み取り/書き込みアクセス許可が引き続き付与されます。 再度、 **SaveChanges**を呼び出すことができます。 KEEP_OPEN_READONLY フラグを渡すか、KEEP_OPEN_SUFFIX を使用してフラグを設定する必要はありません。 
  
プロバイダーが KEEP_OPEN_READWRITE フラグをサポートしているかどうかは、プロバイダーの実装によって異なります。 
  
**SaveChanges**が**IUnknown:: Release**の後にのみオブジェクトで行われる呼び出しを示すには、 _ulflags_パラメーターにフラグを設定しません。 **SaveChanges**からのエラーは、保留中の変更を永続的にできないことを示します。 さまざまなプロバイダーが、 **SaveChanges**呼び出しでのフラグの欠落を異なる方法で処理します。 プロバイダーによっては、この状態を KEEP_OPEN_READONLY と同じものとして扱います。他のプロバイダーは、KEEP_OPEN_READWRITE と同じように解釈します。 その他のプロバイダーは、 **SaveChanges**呼び出しでフラグを受信しない場合、そのオブジェクトをシャットダウンします。 
  
一部のプロパティ (通常は計算プロパティ) は、 **SaveChanges**を呼び出し、場合によっては**解放**されるまで処理できません。
  
添付ファイルを複数のメッセージに保存するなどの一括変更を行う場合は、 _ulflags_で MAPI_DEFERRED_ERRORS フラグを設定することにより、エラー処理を延期します。 複数の添付ファイルを複数のメッセージに保存する場合は、各添付ファイルに**savechanges**呼び出しを1つずつ、各メッセージに**savechanges**呼び出しを1つ行います。 添付ファイルの各呼び出しに対して MAPI_DEFERRED_ERRORS フラグを設定し、最後のメッセージ以外のすべてのメッセージに対して設定します。 
  
**SaveChanges**が MAPI_E_OBJECT_CHANGED を返す場合は、元のオブジェクトが変更されていないかどうかを確認します。 その場合は、変更によって以前の変更を上書きするか、別の場所に保存するかをユーザーに警告します。 元のオブジェクトが削除されている場合は、オブジェクトを別の場所に保存する機会をユーザーに提供するようにユーザーに警告します。 
  
開いているオブジェクトが削除されている場合、FORCE_SAVE フラグを使用して**SaveChanges**を呼び出すことはできません。 
  
**SaveChanges**がエラーを返す場合、 _ulflags_パラメーターに設定されているフラグに関係なく、変更を保存しようとしたオブジェクトは開いたままになります。 
  
> [!IMPORTANT]
> _ulflags_ NON_EMS_XP_SAVE および SPAMFILTER_ONSAVE は、現在のダウンロード可能なヘッダーファイルでは定義されていない場合があります。その場合は、次の値を使用してコードに追加できます。 >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
詳細については、「 [MAPI プロパティの保存](saving-mapi-properties.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI プロパティの保存](saving-mapi-properties.md)

