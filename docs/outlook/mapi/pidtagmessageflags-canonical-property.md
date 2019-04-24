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
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325744"
---
# <a name="pidtagmessageflags-canonical-property"></a>PidTagMessageFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの送信元と現在の状態を示すフラグのビットマスクを含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|識別子:  <br/> |0x0E07  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、送信側と受信側の両方で公開されている、クライアントアプリケーションまたはストアプロバイダーによって異なる値を持つ、送信側と受信側のメッセージプロパティです。 このプロパティは、メッセージが最初に作成されて保存されてから、メッセージストアプロバイダー、トランスポートプロバイダー、およびメッセージが処理されるときに MAPI スプーラーによって定期的に更新されるときに、クライアントまたはメッセージストアプロバイダーによって初期化されます。メッセージの処理とその状態変更. 
  
このプロパティは、送信前と送信後のメッセージ、および受信したメッセージのすべてのコピーに存在します。 受信者のプロパティではありませんが、受信者によって開封または変更されたかどうかに応じて、各受信者に公開されます。 
  
このプロパティには、次の1つ以上のフラグを設定できます。
  
MSGFLAG_ASSOCIATED 
  
> メッセージはフォルダーの関連付けられたメッセージです。 クライアントまたはプロバイダーは、このフラグに対して読み取り専用アクセス権を持っています。 関連付けられたメッセージの場合、MSGFLAG_READ フラグは無視されます。読み取り/未開封の状態は保持されません。 
    
MSGFLAG_FROMME 
  
> メッセージを送信したメッセージングユーザーがメッセージを受信しました。 クライアントまたはプロバイダーは、このフラグへの読み取り/書き込みアクセス権を持ちます。その後、最初の[imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しに対しては読み取り専用になります。 このフラグは、トランスポートプロバイダーによって設定されることを目的としています。 
    
MSGFLAG_HASATTACH 
  
> メッセージに添付ファイルが1つ以上ある。 このフラグは、メッセージの**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) プロパティに対応します。 クライアントは、このフラグへの読み取り専用アクセス権を持っています。 
    
MSGFLAG_NRN_PENDING 
  
> メッセージに対して未読レポートを送信する必要があります。 クライアントまたはプロバイダーは、このフラグに対して読み取り専用アクセス権を持っています。 
    
MSGFLAG_ORIGIN_INTERNET 
  
> 受信メッセージがインターネット経由で到着しました。 これは、組織外またはソースからのものであり、ゲートウェイは信頼を考慮できません。 クライアントは、ユーザーに適切なメッセージを表示する必要があります。 トランスポートプロバイダーはこのフラグを設定します。クライアントは読み取り専用のアクセス権を持っています。 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> 受信メッセージが、X またはインターネット以外の外部リンク経由で到着しました。 これは、組織外またはソースからのものであり、ゲートウェイは信頼を考慮できません。 クライアントは、ユーザーに適切なメッセージを表示する必要があります。 トランスポートプロバイダーはこのフラグを設定します。クライアントは読み取り専用のアクセス権を持っています。 
    
MSGFLAG_ORIGIN_X400 
  
> 受信したメッセージが、X. 400 リンクを介して到着しました。 これは、組織外またはソースからのものであり、ゲートウェイは信頼を考慮できません。 クライアントは、ユーザーに適切なメッセージを表示する必要があります。 トランスポートプロバイダーはこのフラグを設定します。クライアントは読み取り専用のアクセス権を持っています。 
    
MSGFLAG_READ 
  
> メッセージに開封済みのマークが付けられています。 これは、いつでも[IMessage:: setreadflag](imessage-setreadflag.md)または[imapifolder:: setreadflag](imapifolder-setreadflags.md)への呼び出しの結果として発生することがあります。 また、クライアントは、メッセージが初めて保存される前に、メッセージの**imapiprop:: setprops**メソッドを呼び出して、このフラグを設定することもできます。 **MSGFLAG_ASSOCIATED**フラグが設定されている場合、このフラグは無視されます。 
    
MSGFLAG_RESEND 
  
> メッセージには、配信不能レポートを伴う再送信操作の要求が含まれています。 クライアントまたはプロバイダーは、このフラグへの読み取り/書き込みアクセス権を持ちます。その後、最初の[imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しに対しては読み取り専用になります。 
    
MSGFLAG_RN_PENDING 
  
> メッセージに対して閲覧レポートを送信する必要があります。 クライアントまたはプロバイダーは、このフラグに対して読み取り専用アクセス権を持っています。 
    
MSGFLAG_SUBMIT 
  
> このメッセージは、 [IMessage:: submitmessage](imessage-submitmessage.md)の呼び出しの結果として送信するようにマークされています。 メッセージストアプロバイダーはこのフラグを設定します。クライアントは読み取り専用のアクセス権を持っています。 
    
MSGFLAG_UNMODIFIED 
  
> 送信メッセージは、最初に保存された時点以降変更されていません。受信メッセージは、配信されてから変更されていません。 
    
MSGFLAG_UNSENT 
  
> メッセージがまだ構成されています。 このファイルは保存されますが、送信されていません。 クライアントまたはプロバイダーは、このフラグへの読み取り/書き込みアクセス権を持ちます。その後、最初の[imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しに対しては読み取り専用になります。 クライアントがメッセージの送信時にこのフラグを設定していない場合、メッセージストアプロバイダーは**IMessage:: submitmessage**が呼び出されたときにこのフラグを設定します。 通常、このフラグはメッセージが送信された後にクリアされます。 
    
クライアントまたはメッセージストアプロバイダーは、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出してフラグ値を読み取ることによって、メッセージの現在の状態をいつでも確認できます。 クライアントまたはプロバイダーは、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、現在読み取り/書き込みアクセス権を持つフラグを変更することもできます。 
  
フラグのいくつかは常に値の取得のみ可能です。 一部のプロパティは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを最初に呼び出したときまでは読み取り/書き込みが行われ、それ以降は**imapiprop:: setprops**に関しては読み取り専用になります。 MSGFLAG_READ の1つは、後で[IMessage:: setreadflag](imessage-setreadflag.md)または[imapifolder:: setreadflag](imapifolder-setreadflags.md)を使用して変更できます。 
  
通常、このプロパティの初期値は MSGFLAG_UNSENT と MSGFLAG_UNMODIFIED で、まだ送信または変更されていないメッセージを示します。 メッセージが2回目に保存されると、メッセージストアプロバイダーは MSGFLAG_UNMODIFIED フラグをクリアします。 メッセージを保存するときにメッセージストアプロバイダーが設定できるもう1つの値は、MSGFLAG_HASATTACH フラグで、メッセージに1つ以上の添付ファイルがあることを示します。 **PR_HASATTACH**プロパティは、この設定値から計算されます。 
  
クライアントが[IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出してメッセージを送信すると、メッセージストアプロバイダーは MAPI スプーラー用のコピーを作成し、MSGFLAG_SUBMIT フラグを設定してこのプロパティを更新します。 まだ設定されていない場合、メッセージストアプロバイダーは MSGFLAG_UNSENT も設定します。 MSGFLAG_SUBMIT は、 **** 送信処理を開始し、メッセージがクライアントに対して読み取り専用になっていることを示します。 MSGFLAG_UNSENT は、MAPI スプーラーがメッセージを処理していることを示します。 送信プロセスが取り消されると、メッセージストアプロバイダーはこのフラグをリセットします。 
  
メッセージが配信のためにトランスポートプロバイダーに渡されると、送信者がメッセージの受信時にメッセージングサーバーと同じアカウントを持っていた場合、トランスポートプロバイダーは MSGFLAG_FROMME フラグを設定します。 トランスポートプロバイダー現在ログオンしているユーザーによって送信された受信メッセージに対して MSGFLAG_FROMME を設定します。 クライアントは、この値を使用して、[送信済みアイテム] フォルダーのコンテンツテーブルに [送信者名] よりも、受信者名を表示することが適切であるかどうかを判断できます。 構成処理中に保存されてまだ送信されていないメッセージも、送信者名ではなく受信者名で表示されます。 
  
受信メッセージの場合、メッセージストアプロバイダーは、MSGFLAG_READ フラグをクリアしてその読み取り状態をリセットします。 クライアントは、メッセージの[IMessage:: setreadflag](imessage-setreadflag.md)メソッドまたはそのフォルダーの imapifolder を呼び出して、読み取り状態を変更し、読み取りおよび非開封レポートの送信を制御する必要がある場合に、MSGFLAG_READ フラグを設定またはクリアできます[。setreadflags](imapifolder-setreadflags.md)メソッド。 これらのメソッドの主な違いは、フォルダーメソッドがフォルダー内の1つ、複数、またはすべてのメッセージに影響する可能性があることです。 message メソッドは、1つのメッセージに影響します。 
  
クライアントは、MSGFLAG_ORIGIN_X400、MSGFLAG_ORIGIN_INTERNET、および MSGFLAG_ORIGIN_MISC_EXT フラグの受信メッセージもテストする必要があります。 これらのフラグは、受信トランスポートプロバイダーによって設定され、ゲートウェイが信頼を考慮できない送信元から届いたメッセージを示します。 これは、メッセージが組織外にあるか、内部ではゲートウェイで認識されないワークステーションから発信されたことを意味します。 いずれの場合も、送信者の id は確認されず、コンピューターウイルスが組織に導入される危険性があります。 クライアントは警告メッセージをユーザーに表示し、それを開かずにメッセージを削除するオプションを提供します。 
  
メッセージストアプロバイダーは、受信メッセージの MSGFLAG_UNMODIFIED フラグを設定します。 MSGFLAG_UNMODIFIED は、メッセージが配信後に変更されていないことを示します。 クライアントは、メッセージストアプロバイダーによって設定された後に、この値をクリアすることはできません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

