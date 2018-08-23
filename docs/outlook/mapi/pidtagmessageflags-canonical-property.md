---
title: PidTagMessageFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageFlags
api_type:
- HeaderDef
ms.assetid: 7561112b-ca72-4c49-a8a0-cc1879a4e151
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f2e565dc8137edee441643a5d02a154f78737099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802990"
---
# <a name="pidtagmessageflags-canonical-property"></a>PidTagMessageFlags 標準プロパティ

  
  
**適用対象**: Outlook 
  
原点とメッセージの現在の状態を示すフラグのビットマスクを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|識別子:  <br/> |0x0E07  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、送信側と関連するクライアント アプリケーションまたはストア プロバイダーによって値が異なると、転送の終了を受信の両方で公開されている nontransmittable メッセージ プロパティです。 このプロパティは、状態メッセージが作成され、最初に保存しし、定期的に更新されるメッセージ ストア プロバイダー、トランスポート プロバイダーでは、MAPI スプーラーによってメッセージが処理されるときにクライアントまたはメッセージのストア プロバイダーを初期化します。変更します。 
  
このプロパティには、両方の前後に、送信メッセージと受信したメッセージのすべてのコピーが存在しています。 受信者のプロパティではありませんが、方法が異なるかどうかを読み取るまたはされた受取人が変更に従って、各受信者に公開されます。 
  
次のフラグの 1 つ以上は、このプロパティを設定できます。
  
MSGFLAG_ASSOCIATED 
  
> メッセージは、フォルダーの関連するメッセージです。 クライアントまたはプロバイダーは、このフラグを読み取り専用のアクセスを持っています。 開封/未開封状態は保持されません、関連付けられているメッセージでは、MSGFLAG_READ フラグは無視されます。 
    
MSGFLAG_FROMME 
  
> メッセージング ユーザーの送信メッセージを受信するメッセージング ユーザーがいました。 クライアントまたはプロバイダーがこのフラグを読み取り/書き込みアクセス読み取り専用と[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の最初の呼び出しまでその後。 このフラグは、トランスポート プロバイダーによって設定されるものです。 
    
MSGFLAG_HASATTACH 
  
> メッセージには、少なくとも 1 つの添付ファイルがあります。 このフラグは、メッセージの**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) のプロパティに対応します。 クライアントでは、このフラグを読み取り専用のアクセスがあります。 
    
MSGFLAG_NRN_PENDING 
  
> Nonread レポートは、メッセージを送信する必要があります。 クライアントまたはプロバイダーは、このフラグを読み取り専用のアクセスを持っています。 
    
MSGFLAG_ORIGIN_INTERNET 
  
> インターネット経由で受信したメッセージが到着しました。 組織の外部またはゲートウェイが考えることはできません信頼できるソースから発生します。 クライアントは、ユーザーに適切なメッセージを表示する必要があります。 トランスポート プロバイダーは、このフラグを設定します。クライアントでは、読み取り専用アクセスがあります。 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> 外部リンク以外は、X.400、またはインターネット経由で受信したメッセージが到着しました。 組織の外部またはゲートウェイが考えることはできません信頼できるソースから発生します。 クライアントは、ユーザーに適切なメッセージを表示する必要があります。 トランスポート プロバイダーは、このフラグを設定します。クライアントでは、読み取り専用アクセスがあります。 
    
MSGFLAG_ORIGIN_X400 
  
> X.400 リンク経由で受信したメッセージが到着しました。 組織の外部またはゲートウェイが考えることはできません信頼できるソースから発生します。 クライアントは、ユーザーに適切なメッセージを表示する必要があります。 トランスポート プロバイダーは、このフラグを設定します。クライアントでは、読み取り専用アクセスがあります。 
    
MSGFLAG_READ 
  
> メッセージは読み取りとしてマークします。 これは、 [IMessage::SetReadFlag](imessage-setreadflag.md)または[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)任意の時点の呼び出しの結果として発生します。 クライアントは、最初にメッセージを保存する前に、メッセージの**IMAPIProp::SetProps**メソッドを呼び出すことによってこのフラグを設定することもできます。 **MSGFLAG_ASSOCIATED**フラグが設定されている場合、このフラグは無視されます。 
    
MSGFLAG_RESEND 
  
> メッセージには、配信不能レポートの再送信の操作の要求が含まれています。 クライアントまたはプロバイダーがこのフラグを読み取り/書き込みアクセス読み取り専用と[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の最初の呼び出しまでその後。 
    
MSGFLAG_RN_PENDING 
  
> リードのレポートは、メッセージを送信する必要があります。 クライアントまたはプロバイダーは、このフラグを読み取り専用のアクセスを持っています。 
    
MSGFLAG_SUBMIT 
  
> [IMessage::SubmitMessage](imessage-submitmessage.md)への呼び出しの結果を送信するメッセージをマークします。 メッセージ ストア プロバイダーは、このフラグを設定します。クライアントでは、読み取り専用アクセスがあります。 
    
MSGFLAG_UNMODIFIED 
  
> 送信メッセージが保存されている最初の時点から変更されていません。配信された後に受信したメッセージが変更されていません。 
    
MSGFLAG_UNSENT 
  
> メッセージは、まだ構成されています。 保存されますが、まだ送信されていません。 クライアントまたはプロバイダーがこのフラグを読み取り/書き込みアクセス読み取り専用と[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の最初の呼び出しまでその後。 クライアントがメッセージの送信時にこのフラグを設定しない場合は、メッセージ ストア プロバイダーを設定、 **IMessage::SubmitMessage**が呼び出されたときにします。 通常、メッセージが送信された後、このフラグはクリアされます。 
    
クライアントまたはメッセージ ストア プロバイダーは、フラグの値を読み取るための[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すことによって、いつでも、メッセージの現在の状態を確認できます。 クライアントまたはプロバイダーでは、現在読み取り/書き込みアクセス権を持つ任意のフラグを変更するのには[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すこともできます。 
  
フラグのいくつかは常に読み取り専用です。 限り**IMAPIProp::SetProps**は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッド、およびその後の最初の呼び出しに読み取り専用になるまでは読み取り/書き込みがあります。 、MSGFLAG_READ、これらの 1 つは、 [IMessage::SetReadFlag](imessage-setreadflag.md)または[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)を後で変更できます。 
  
このプロパティの初期値は通常は、送信または変更されたされていないメッセージを示すには、MSGFLAG_UNSENT と MSGFLAG_UNMODIFIED。 2 回目のメッセージが保存されると、メッセージ ストア プロバイダーは、MSGFLAG_UNMODIFIED フラグをクリアします。 メッセージ ストア プロバイダーがメッセージを保存するときに設定できる別の値は、MSGFLAG_HASATTACH フラグをメッセージに 1 つまたは複数の添付ファイルがあることを示します。 **PR_HASATTACH**プロパティは、この設定から計算されます。 
  
クライアントがメッセージを送信する[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出すと、メッセージ ストア プロバイダー コピーでは、MAPI スプーラーを無効になり、MSGFLAG_SUBMIT フラグを設定することによってこのプロパティを更新します。 メッセージ ストア プロバイダーは、まだ設定されていない場合にも MSGFLAG_UNSENT を設定します。 MSGFLAG_SUBMIT であることを示します**SubmitMessage**が呼び出されると、送信プロセスを開始し、メッセージがクライアントに読み取り専用です。 MSGFLAG_UNSENT では、MAPI スプーラーがメッセージを処理していることを示します。 送信処理がキャンセルされた場合、メッセージ ストア プロバイダーは、このフラグをリセットします。 
  
配信用のトランスポート プロバイダーにメッセージを指定すると場合送信元メッセージング サーバーで同じアカウントでメッセージを受信しましたと、トランスポート プロバイダーは、MSGFLAG_FROMME フラグを設定します。 トランスポート プロバイダーは、現在ログオンしているユーザーから送信された受信メッセージの MSGFLAG_FROMME を設定します。 クライアントは、送信者の名前よりも [送信済みアイテム フォルダーの内容の表に受取人の名前を表示するのに方が適切であると判断するのには、この値を使用できます。 構成処理中に保存して送信されていないメッセージは、送信者の名前ではなく、受信者の名前を使用しても表示されます。 
  
着信メッセージの場合は、メッセージ ストア プロバイダーは、読み取りの状態をリセットするのには MSGFLAG_READ フラグをクリアします。 クライアントを設定または読み取りステータスを変更して、メッセージの[IMessage::SetReadFlag](imessage-setreadflag.md)メソッドまたはそのフォルダーの[IMAPIFolder のいずれかを呼び出すことにより、読み取りおよび nonread のレポートの送信を制御する必要がある場合、MSGFLAG_READ フラグをオフにできます。SetReadFlags](imapifolder-setreadflags.md)メソッドです。 これらのメソッドを実装するには、オブジェクト以外のオブジェクトの主な違いは、フォルダー メソッドは、1 つ、複数、またはすべてのフォルダーにメッセージに影響ことができます。 メッセージのメソッドでは、1 つのメッセージに影響します。 
  
クライアントも MSGFLAG_ORIGIN_X400、MSGFLAG_ORIGIN_INTERNET、および MSGFLAG_ORIGIN_MISC_EXT のフラグを受信したメッセージをテストしてください。 これらのフラグは、受信トランスポート プロバイダーによって設定され、ゲートウェイが信頼関係を考慮することはできませんが、ソースからメッセージが到着したことを示します。 つまり、メッセージの送信元組織外にあるか、または内部的にですが、ゲートウェイとわかっていないワークステーションから。 どのような場合は、送信者の身元を確認することがない可能性がありますと、組織内にコンピューター ウイルスを導入する際のリスクがあります。 クライアントは、ユーザーに警告メッセージを表示し、開かずにメッセージを削除するオプションを提供する必要があります。 
  
メッセージ ストア プロバイダーは、受信メッセージの MSGFLAG_UNMODIFIED フラグを設定します。 MSGFLAG_UNMODIFIED は、メッセージが配信以降変更されていないことを示します。 メッセージ ストア プロバイダーによって設定された後、クライアントはこの値をクリアできません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

