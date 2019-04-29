---
title: 1回限りのテーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: 8719536efa9bffb1226f8fb665b912eb872227f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439528"
---
# <a name="one-off-tables"></a>1回限りのテーブル

**適用対象**: Outlook 2013 | Outlook 2016 
  
1回限りのテーブルには、アドレス帳プロバイダーが新しい受信者を作成する際にサポートするテンプレートに関する情報が含まれます。 1回限りのテーブルは、アドレス帳プロバイダー、個別のアドレス帳コンテナー、および MAPI によって実装され、永続的または一時的なものにすることができます。 
  
> [!NOTE]
> 1回限りのテーブルのテンプレートをテンプレート識別子と混同しないでください。これらの用途は似ていますが、コードの構成要素は同じではありません。 テンプレートは、特定の種類の受信者を作成するために使用されますが、テンプレート識別子は、ホストプロバイダーに属する1つの受信者のデータを、外部プロバイダーに属する別の受信者をサポートするコードでバインドするために使用されます。 
  
クライアントが新しい受信者を作成します。
  
- 送信メッセージの受信者の一覧に追加します。
    
- アドレス帳のいずれかのコンテナーに追加します。
    
どちらの場合も、アドレス帳プロバイダーは、1回限りのテーブルを返すように要求されます。 アドレス帳プロバイダーは、両方の状況で使用される単一の1回限りのテーブルを実装するか、状況ごとに一意の1回限りのテーブルを実装できます。 
  
送信メッセージに受信者が含まれる場合、MAPI はアドレス帳プロバイダーの[IABLogon:: getoneofftable](iablogon-getoneofftable.md)メソッドを呼び出して、その1回限りのテーブルを取得します。 1回限りのテーブルには、有効なアドレスを持つ受信者を作成した結果として、ユーザーが情報を入力できるテンプレートが含まれています。 MAPI は、このテーブルで通知を登録し、変更内容をユーザーに反映させるために開いたままにします。 MAPI は、サブシステムまたはアドレス帳状態オブジェクトの[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドが呼び出されたときにのみテーブルを解放します。 
  
受信者がコンテナーに追加されると、MAPI は別の呼び出しを実行し、コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、その**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを取得します。 この1回限りのテーブルに含まれるテンプレートのセットは、コンテナーに追加できる受信者の種類を表します。 たとえば、メールサーバーは、多くの場合、インストールされているゲートウェイごとに1つのコンテナーを公開するので、各コンテナーは対応するゲートウェイに固有のアドレスのみを保持することができます。
  
MAPI は、独自のテンプレートと、セッション内の各アドレス帳プロバイダーからのテンプレートを含む、1回限りのテーブルを提供します。 MAPI には、ユーザーがその形式を知っていると仮定して、任意のアドレスの種類に対して新しい受信者を作成するために使用できる汎用テンプレートが用意されています。 アドレス帳プロバイダー[は、imapisupport:: getoneofftable](imapisupport-getoneofftable.md)を呼び出して、この1回限りのテーブルを使用します。 MAPI の1回限りのテーブルに含まれている各テンプレートは、有効な受信者のアドレスを持つ受信者を作成します。
  
通常、アドレス帳プロバイダーは、サポートするアドレスの種類ごとに1つのテンプレートを提供します。 ただし、テンプレートをサポートする必要はありません。 新しいアドレスの作成が許可されていないアドレス帳プロバイダーは、MAPI が1回限りのテーブルを要求するために MAPI_E_NO_SUPPORT を返すことがあります。 アドレス帳プロバイダーは、新しいアドレスの作成を許可していますが、テンプレートを指定しない場合は、MAPI の1回限りのテーブルにリストされているテンプレートを使用するために**imapisupport:: getoneofftable**を呼び出すことができます。 
  
次のプロパティは、1回限りのテーブルで必要な列セットを作成します。
  
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE**([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE**は、テンプレートを使用して作成された新しい受信者に関連付けることができるアドレスの種類を示します。 
  
 **PR_DISPLAY_NAME**および**PR_DISPLAY_TYPE**は、新しい受信者とデータを関連付けます。 **PR_DISPLAY_NAME**には、新しい受信者を識別する文字列が含まれています。 **PR_DISPLAY_TYPE**には、行に表示されるアイコンの種類を識別する定数が含まれています。 メッセージングユーザーのテンプレートは、 **PR_DISPLAY_TYPE**列が DT_MAILUSER に設定されています。配布リストのテンプレートでは、 **PR_DISPLAY_TYPE**列が DT_DISTLIST に設定されています。 
  
 **PR_ENTRYID**は、新しい受信者を作成するために使用するテンプレートのエントリ識別子です。 このエントリ識別子は、今後の[IAddrBook:: newentry](iaddrbook-newentry.md)、 [IAddrBook:: openentry](iaddrbook-openentry.md)、および[IABContainer:: createentry](iabcontainer-createentry.md)呼び出しに渡すことができます。 コンテナーは、既定のメッセージングユーザーテンプレートの行の**PR_ENTRYID**列を**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) に設定し、既定の配布リストの行の**PR_ENTRYID**列に設定します。テンプレートを**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) にします。 
  
 **PR_DEPTH**は、テンプレートのインデントレベルを示すことによって、1回限りのテーブル内のエントリの階層的な表示をサポートするために使用されます。 1回限りのテーブルをフラットリストとして表示することも、階層表示することもできますが、後者の方が推奨され、アドレス帳プロバイダーは各行の**PR_DEPTH**列を適切に設定してサポートする必要があります。 **PR_DEPTH**は0から始まります。**PR_DEPTH**列の値が0の行はインデントされません。 **PR_DEPTH**の値が大きいほど、行がインデントされます。 たとえば、 **PR_DEPTH**が1に設定されている行は1つのタブにインデントされ、 **PR_DEPTH**が3に設定されている行は3つのタブにインデントされます。 
  
 **PR_SELECTABLE**は、テーブル内の行が、選択して、新しい受信者を作成するために使用できるテンプレートを表しているかどうかを示すために使用されます。 1回限りのテーブルのほとんどの行はテンプレートを表していますが、プロバイダーにはテンプレート以外の行を含めることができます。 たとえば、プロバイダーは、表示に表示されるカテゴリ行を含む、テンプレートの種類によって、1回限りのテーブルを整理する必要がありますが、受信者の作成には使用されません。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

