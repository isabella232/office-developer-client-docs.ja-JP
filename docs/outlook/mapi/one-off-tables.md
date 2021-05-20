---
title: One-Offテーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: 8719536efa9bffb1226f8fb665b912eb872227f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439528"
---
# <a name="one-off-tables"></a>One-Offテーブル

**適用対象**: Outlook 2013 | Outlook 2016 
  
1 回のテーブルには、アドレス帳プロバイダーが新しい受信者の作成にサポートするテンプレートに関する情報が含まれる。 一時テーブルは、アドレス帳プロバイダー、個々のアドレス帳コンテナー、MAPI によって実装され、永続的または一時的な場合があります。 
  
> [!NOTE]
> 一時テーブル内のテンプレートとテンプレート識別子を混同しない。目的は似ていますが、コード構造は似ていません。 テンプレートは、特定の種類の受信者を作成するために使用されます。一方、テンプレート識別子は、外部プロバイダーに属する別の受信者をサポートするコードを持つホスト プロバイダーに属する 1 つの受信者のデータをバインドするために使用されます。 
  
クライアントは新しい受信者を作成します。
  
- 送信メッセージの受信者リストに追加します。
    
- アドレス帳のコンテナーの 1 つに追加します。
    
どちらのシナリオでも、アドレス帳プロバイダーは 1 回きりテーブルを返す必要があります。 アドレス帳プロバイダーは、両方の状況で使用する単一の 1 回表または状況ごとに一意の 1 回表を実装できます。 
  
受信者が送信メッセージに含まれる場合、MAPI はアドレス帳プロバイダーの [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) メソッドを呼び出して、一時テーブルを取得します。 一時テーブルには、有効なアドレスを持つ受信者が作成される情報をユーザーが入力できるテンプレートが含まれています。 MAPI は、変更をユーザーに反映できるよう、このテーブルの通知を開いた状態で登録します。 MAPI は、サブシステムまたはアドレス帳の状態オブジェクトの [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドが呼び出された場合にのみ、テーブルを解放します。 
  
受信者がコンテナーに追加される場合、MAPI は別の呼び出しを行い、コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出して、PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを取得します。 この一時テーブルに含まれるテンプレートのセットは、コンテナーに追加できる受信者の種類を表します。 たとえば、メール サーバーは多くの場合、インストールされているゲートウェイごとに 1 つのコンテナーを公開して、各コンテナーが対応するゲートウェイに固有のアドレスのみを保持します。
  
MAPI には、セッション内の各アドレス帳プロバイダーのテンプレートと同様に、独自のテンプレートを含む 1 回限りのテーブルが用意されています。 MAPI は、ユーザーが形式を知っていると仮定して、任意のアドレスの種類の新しい受信者を作成するために使用できる汎用テンプレートを提供します。 アドレス帳プロバイダーは [、IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)を呼び出すことによって、この一時テーブルを使用します。 MAPI の一時表に含まれる各テンプレートは、有効な受信者アドレスを持つ受信者を作成します。
  
アドレス帳プロバイダーは、通常、サポートするアドレスの種類ごとに 1 つのテンプレートを提供します。 ただし、テンプレートのサポートは必要ありません。 新しいアドレスの作成を許可しないアドレス帳プロバイダーは、MAPI が 1 回MAPI_E_NO_SUPPORT要求するときにアドレス帳を返す可能性があります。 新しいアドレスの作成を許可するが、テンプレートを指定しないアドレス帳プロバイダーは **、IMAPISupport::GetOneOffTable** を呼び出して、MAPI の一時テーブルに記載されているテンプレートを使用できます。 
  
次のプロパティは、1 回のテーブルで必要な列セットを構成します。
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE** テンプレートで作成された新しい受信者に関連付けられるアドレスの種類を示します。 
  
 **PR_DISPLAY_NAME****とPR_DISPLAY_TYPE** を新しい受信者に関連付ける必要があります。 **PR_DISPLAY_NAME** には、新しい受信者を識別する文字列が含まれます **。PR_DISPLAY_TYPE** には、行と一緒に表示するアイコンの種類を識別する定数が含まれます。 メッセージング ユーザー用のテンプレートには、PR_DISPLAY_TYPE **列が** 設定DT_MAILUSER。配布リストのテンプレートの列は **、PR_DISPLAY_TYPEに設定** DT_DISTLIST。 
  
 **PR_ENTRYID** は、新しい受信者の作成に使用するテンプレートのエントリ識別子です。 このエントリ識別子は、将来の[IAddrBook::NewEntry、IAddrBook::OpenEntry、](iaddrbook-openentry.md)[および IABContainer::CreateEntry](iabcontainer-createentry.md)呼び出しに渡されます。 [](iaddrbook-newentry.md) コンテナーは、既定のメッセージング ユーザー テンプレートの行の **PR_ENTRYID** 列を **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) に設定し、既定の配布リスト テンプレートの行の **PR_ENTRYID** 列を **PR_DEF_CREATE_DL** ([PidTagDefCreateDl)](pidtagdefcreatedl-canonical-property.md)に設定します。 
  
 **PR_DEPTH** は、テンプレートのインデントのレベルを示して、1 回のテーブル内のエントリの階層表示をサポートするために使用されます。 1 回限りテーブルはフラット リストまたは階層表示として表示することができますが、後者が望ましく、アドレス帳プロバイダーは行ごとに **PR_DEPTH** 列を適切に設定してサポートする必要があります。 **PR_DEPTH** はゼロベースです。列の値が 0 の **行PR_DEPTHインデント** されません。 値が大 **きいほどPR_DEPTH** 行がインデントされます。 たとえば、1 に設定 **PR_DEPTH** 行は 1 つのタブにインデントされ、3 に設定された行は 3 **つのタブPR_DEPTH** インデントされます。 
  
 **PR_SELECTABLE** は、テーブル内の行が、新しい受信者を作成するために選択して使用できるテンプレートを表すかどうかを示すために使用されます。 1 回表のほとんどの行はテンプレートを表しますが、プロバイダーにはテンプレート以外の行を含めできます。 たとえば、プロバイダーは、表示に表示されるが受信者の作成には使用されないカテゴリ行を含む、テンプレートの種類別に 1 回のテーブルを整理できます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

