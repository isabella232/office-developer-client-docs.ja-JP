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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325744"
---
# <a name="pidtagmessageflags-canonical-property"></a>PidTagMessageFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの発生元と現在の状態を示すフラグのビットマスクが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|識別子:  <br/> |0x0E07  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、送信の送信側と受信側の両方で公開される送信不可のメッセージ プロパティで、クライアント アプリケーションまたはストア プロバイダーに応じて異なる値を使用します。 このプロパティは、メッセージが初めて作成および保存され、メッセージが処理され、状態が変更されると、メッセージ ストア プロバイダー、トランスポート プロバイダー、MAPI スプーラーによって定期的に更新されると、クライアントまたはメッセージ ストア プロバイダーによって初期化されます。 
  
このプロパティは、送信の前と送信後の両方のメッセージと、受信したメッセージのすべてのコピーに存在します。 受信者プロパティではありませんが、受信者によって読み取りまたは変更されたかどうかに応じて、各受信者に対して異なる方法で公開されます。 
  
このプロパティには、次のフラグを 1 つ以上設定できます。
  
MSGFLAG_ASSOCIATED 
  
> メッセージは、フォルダーの関連付けられたメッセージです。 クライアントまたはプロバイダーには、このフラグへの読み取り専用アクセス権があります。 関連MSGFLAG_READ、読み取り/未読状態を保持しない場合、このフラグは無視されます。 
    
MSGFLAG_FROMME 
  
> 送信するメッセージング ユーザーは、メッセージを受信するメッセージング ユーザーでした。 クライアントまたはプロバイダーは、最初の [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 呼び出しまでこのフラグへの読み取り/書き込みアクセス権を持ち、その後は読み取り専用です。 このフラグは、トランスポート プロバイダーによって設定することを意図しています。 
    
MSGFLAG_HASATTACH 
  
> メッセージには少なくとも 1 つの添付ファイルがあります。 このフラグは、メッセージのプロパティ ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md) **)** PR_HASATTACHに対応します。 クライアントには、このフラグへの読み取り専用アクセス権があります。 
    
MSGFLAG_NRN_PENDING 
  
> メッセージに対して読み取り以外のレポートを送信する必要があります。 クライアントまたはプロバイダーには、このフラグへの読み取り専用アクセス権があります。 
    
MSGFLAG_ORIGIN_INTERNET 
  
> 受信メッセージがインターネット上に到着しました。 これは、組織外またはゲートウェイが信頼できると見なすソースのいずれかから発生します。 クライアントは、ユーザーに適切なメッセージを表示する必要があります。 トランスポート プロバイダーは、このフラグを設定します。クライアントには読み取り専用アクセス権があります。 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> 受信メッセージは、X.400 またはインターネット以外の外部リンクを通して届きました。 これは、組織外またはゲートウェイが信頼できると見なすソースのいずれかから発生します。 クライアントは、ユーザーに適切なメッセージを表示する必要があります。 トランスポート プロバイダーは、このフラグを設定します。クライアントには読み取り専用アクセス権があります。 
    
MSGFLAG_ORIGIN_X400 
  
> 受信メッセージが X.400 リンクを越え到着しました。 これは、組織外またはゲートウェイが信頼できると見なすソースのいずれかから発生します。 クライアントは、ユーザーに適切なメッセージを表示する必要があります。 トランスポート プロバイダーは、このフラグを設定します。クライアントには読み取り専用アクセス権があります。 
    
MSGFLAG_READ 
  
> メッセージは読み取り済みとしてマークされます。 これは [、IMessage::SetReadFlag](imessage-setreadflag.md) または [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)への呼び出しの結果として発生する可能性があります。 クライアントは、メッセージが初めて保存される前に、メッセージの **IMAPIProp::SetProps** メソッドを呼び出すことによって、このフラグを設定できます。 このフラグは、このフラグ **がMSGFLAG_ASSOCIATED設定** されている場合は無視されます。 
    
MSGFLAG_RESEND 
  
> メッセージには、非送信レポートを使用した再送信操作の要求が含まれます。 クライアントまたはプロバイダーは、最初の [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 呼び出しまでこのフラグへの読み取り/書き込みアクセス権を持ち、その後は読み取り専用です。 
    
MSGFLAG_RN_PENDING 
  
> メッセージの読み取りレポートを送信する必要があります。 クライアントまたはプロバイダーには、このフラグへの読み取り専用アクセス権があります。 
    
MSGFLAG_SUBMIT 
  
> メッセージは [、IMessage::SubmitMessage](imessage-submitmessage.md)への呼び出しの結果として送信用にマークされます。 メッセージ ストア プロバイダーは、このフラグを設定します。クライアントには読み取り専用アクセス権があります。 
    
MSGFLAG_UNMODIFIED 
  
> 送信メッセージは、最初に保存された時から変更されていない。受信メッセージは配信後に変更されていない。 
    
MSGFLAG_UNSENT 
  
> メッセージはまだ構成中です。 保存されますが、送信されていない。 クライアントまたはプロバイダーは、最初の [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 呼び出しまでこのフラグへの読み取り/書き込みアクセス権を持ち、その後は読み取り専用です。 メッセージが送信される時点でクライアントがこのフラグを設定しない場合、メッセージ ストア プロバイダーは **IMessage::SubmitMessage** が呼び出されたときにこのフラグを設定します。 通常、このフラグはメッセージの送信後にクリアされます。 
    
クライアントまたはメッセージ ストア プロバイダーは [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出してフラグ値を読み取って、いつでもメッセージの現在の状態を確認できます。 クライアントまたはプロバイダーは [、IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、現在読み取り/書き込みアクセス権を持つフラグを変更できます。 
  
フラグのいくつかは、常に読み取り専用です。 一部は [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドの最初の呼び出しまで読み取り/書き込みであり、 **その後、IMAPIProp::SetProps** に関する限り読み取り専用になります。 これらの 1 つは、MSGFLAG_READ [IMessage::SetReadFlag](imessage-setreadflag.md) または [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)を使用して変更できます。 
  
通常、このプロパティの初期値は、MSGFLAG_UNSENT変更されていないMSGFLAG_UNMODIFIEDメッセージを示すために使用されます。 メッセージが 2 度目に保存される場合、メッセージ ストア プロバイダーはメッセージ MSGFLAG_UNMODIFIEDします。 メッセージの保存時にメッセージ ストア プロバイダーが設定できるもう 1 つの値は、MSGFLAG_HASATTACH フラグで、メッセージに 1 つ以上の添付ファイルが含まれています。 プロパティ **PR_HASATTACH** この設定から計算されます。 
  
クライアントが [IMessage::SubmitMessage](imessage-submitmessage.md) メソッドを呼び出してメッセージを送信すると、メッセージ ストア プロバイダーは MAPI スプーラーのコピーを作成し、MSGFLAG_SUBMIT フラグを設定してこのプロパティを更新します。 メッセージ ストア プロバイダーは、まだ設定されていないMSGFLAG_UNSENTメッセージ ストア プロバイダーも設定します。 MSGFLAG_SUBMIT **SubmitMessage** が呼び出され、送信プロセスが開始され、メッセージがクライアントに対して読み取り専用になります。 MSGFLAG_UNSENT MAPI スプーラーがメッセージを処理中かどうかを示します。 送信プロセスが取り消された場合、メッセージ ストア プロバイダーは、このフラグをリセットします。 
  
メッセージがトランスポート プロバイダーに配信用に与えられると、メッセージが受信されたのと同じアカウントを送信者がメッセージング サーバーに持っていた場合、トランスポート プロバイダーは MSGFLAG_FROMME フラグを設定します。 トランスポート プロバイダーは、MSGFLAG_FROMMEログオンしているユーザーによって送信された受信メッセージのデータを設定します。 クライアントは、この値を使用して、送信者名よりも送信アイテム フォルダーのコンテンツ テーブルに受信者名を表示する方が適切かどうかを判断できます。 構成プロセス中に保存され、まだ送信されていないメッセージは、送信者名ではなく受信者名と一緒に表示する必要があります。 
  
受信メッセージの場合、メッセージ ストア プロバイダーは、MSGFLAG_READフラグをクリアして、読み取り状態をリセットします。 クライアントは、メッセージの [IMessage::SetReadFlag](imessage-setreadflag.md) メソッドまたはフォルダーの [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) メソッドを呼び出すことによって、読み取り状態を変更し、読み取りレポートと非読み取りレポートの送信を制御する必要がある場合に、MSGFLAG_READ フラグを設定またはクリアできます。 これらのメソッドの主な違いは、それらを実装するオブジェクト以外は、フォルダー メソッドがフォルダー内の 1 つ、複数、またはすべてのメッセージに影響を与える可能性がある点です。 message メソッドは、1 つのメッセージに影響します。 
  
クライアントは、受信メッセージをテストして、MSGFLAG_ORIGIN_X400、MSGFLAG_ORIGIN_INTERNET、MSGFLAG_ORIGIN_MISC_EXTする必要があります。 これらのフラグは、受信トランスポート プロバイダーによって設定され、ゲートウェイが信頼できると見なできないソースからメッセージが到着したかどうかを示します。 つまり、メッセージは組織外または内部的に発信されますが、ゲートウェイに対して既知ではないワークステーションから発信されます。 いずれにしても、送信者の身元が確認されない可能性があります。また、コンピューター ウイルスを組織に導入するリスクがあります。 クライアントはユーザーに警告メッセージを表示し、メッセージを開かなくても削除するオプションを提供する必要があります。 
  
メッセージ ストア プロバイダーは、受信メッセージMSGFLAG_UNMODIFIEDフラグを設定します。 MSGFLAG_UNMODIFIEDは、配信後にメッセージが変更されていないかどうかを示します。 クライアントは、メッセージ ストア プロバイダーによって設定された後、この値をクリアできません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

