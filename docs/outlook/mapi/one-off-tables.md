---
title: 1 回限りのテーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0f2040b7-9b6c-4eae-aa68-29c4f7b8bd76
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: fc8d8d53dcbc091df98ba9e23533e4138660c8e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574567"
---
# <a name="one-off-tables"></a>1 回限りのテーブル

**適用されます**: Outlook 2013 |Outlook 2016 
  
一時テーブルには、新しい受信者を作成するため、アドレス帳プロバイダーがサポートしているテンプレートに関する情報が含まれています。 一時テーブルは、アドレス帳プロバイダーは、個々 のアドレス帳コンテナーと MAPI によって実装され、永続的または一時的にすることができます。 
  
> [!NOTE]
> テンプレート識別子を持つ一時テーブルのテンプレートを混同しないでください。それぞれの目的は似ていますが、何も、コード コンス トラクターがいます。 テンプレートを使用して、テンプレートの識別子を使用してデータをバインドする 1 つの受信者の別の受信者をサポートするためにコードのホスト プロバイダーに属している外部のプロバイダーに属している特定の種類の受信者を作成します。 
  
クライアントは、新しい受信者を作成します。
  
- 送信メッセージの受信者の一覧に追加します。
    
- アドレス帳コンテナーの 1 つに追加します。
    
どちらのシナリオでは、アドレス帳プロバイダーは一時テーブルを取得する要求します。 アドレス帳プロバイダーには、両方の状況で使用する 1 つの一時テーブルまたはそれぞれの状況に固有の一時テーブルのいずれかを実装できます。 
  
送信メッセージに含まれる受信者の場合、MAPI は、一時テーブルを取得するために、アドレス帳プロバイダーの[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)メソッドを呼び出します。 一時テーブルには、有効なアドレスを持つ受信者の作成、情報を入力するユーザーを有効にするテンプレートが含まれています。 MAPI レジスタを次の表は、常に通知を開いてユーザーに変更を反映することができますように。 MAPI は、そのサブシステムまたはアドレス帳の状態オブジェクトの[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドが呼び出されたときにのみ、テーブルを解放します。 
  
受信者コンテナーに追加すると MAPI は、コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出し、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを取得するために別の呼び出しを作成します。 この一時テーブルに含まれているテンプレートのセットは、コンテナーに追加できる受信者の種類を表します。 たとえば、メール サーバーでは、多くの場合各コンテナーのみを保持するアドレス、対応するゲートウェイを特定するためにインストールされているすべてのゲートウェイの 1 つのコンテナーを公開します。
  
MAPI は、セッションに独自のテンプレートと同様にそれぞれのアドレス帳プロバイダーからのテンプレートを含む一時テーブルを提供します。 MAPI には、ユーザーがその形式を知っていることを想定しているアドレスの種類の新しい受信者を作成するのに使用できる汎用的なテンプレートが用意されています。 アドレス帳プロバイダーは、 [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)を呼び出すことによって、この一時テーブルを使用します。 各有効な受信者のアドレスを持つ受信者の作成時に MAPI テーブルを 1 回限りの結果に含まれるテンプレートです。
  
アドレス帳プロバイダーは、通常 1 つのテンプレートをサポートしているすべてのアドレスの種類を指定します。 ただし、テンプレートは必要ありませんサポートします。 MAPI 呼び出しを 1 回限りのテーブルを要求すると、新しいアドレスの作成を許可しない、アドレス帳プロバイダーは MAPI_E_NO_SUPPORT を返すことができます。 新しいアドレスの作成を許可する操作を行いますが、任意のテンプレートを指定されていないアドレス帳プロバイダーには、MAPI の一時テーブルに記載されているテンプレートを使用する**IMAPISupport::GetOneOffTable**を呼び出すことができます。 
  
次のプロパティは、必須の列を一時テーブルの設定を構成します。
  
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_SELECTABLE**([PidTagSelectable](pidtagselectable-canonical-property.md))
    
 **PR_ADDRTYPE**は、テンプレートで作成した新しい受信者と関連付けることができるアドレスの種類を示します。 
  
 **PR_DISPLAY_NAME**および**PR_DISPLAY_TYPE**は、新しい受信者にデータを関連付けます。 **PR_DISPLAY_NAME**に新しい受信者を識別する文字列が含まれていて、 **PR_DISPLAY_TYPE**に行を表示するアイコンの種類を識別する定数が含まれています。 メッセージング ユーザーのテンプレートがある、 **PR_DISPLAY_TYPE**列には、DT_MAILUSER です。配布リスト用のテンプレートがある、 **PR_DISPLAY_TYPE**カラムを DT_DISTLIST に設定します。 
  
 **PR_ENTRYID**は、新しい受信者を作成するためのテンプレートのエントリの識別子です。 このエントリ id は、将来の[IAddrBook::NewEntry](iaddrbook-newentry.md)、[アドレス帳コンテナー](iaddrbook-openentry.md)、および[IABContainer::CreateEntry](iabcontainer-createentry.md)の呼び出しに渡すことができます。 コンテナーの既定の**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) に、ユーザー テンプレートと、 **PR_ENTRYID**の行の列の既定の配布リストにメッセージをその行の**PR_ENTRYID**列を設定します。**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) にテンプレートです。 
  
 **PR_DEPTH**は、テンプレートのインデントのレベルを示すことにより、一時テーブルのエントリの階層表示をサポートするために使用されます。 単純なリストまたは階層の表示としては、一時テーブルを表示することができます、ですが、後者をお勧めし、アドレス帳プロバイダーを使用すると行ごとに [ **PR_DEPTH** ] 列を適切に設定することでサポートする必要があります。 **PR_DEPTH**は 0 から始まります。**PR_DEPTH**列の 0 の値を含む行がインデント付きではありません。 **PR_DEPTH**の値が大きいほど、複数の行はインデントではありません。 、 **PR_DEPTH**が 1 に設定を持つ行はインデントが設定された 1 つのタブ 3 に設定された**PR_DEPTH**の行にはインデントが設定された 3 つのタブです。 
  
 **PR_SELECTABLE**を使用すると、テーブル内の行が選択して新しい受信者を作成するために使用できるテンプレートを表すかどうかを指定します。 一時テーブル内のほとんどの行は、テンプレートには、プロバイダーは、非テンプレートの行を含めることができます。 たとえば、プロバイダーはディスプレイに表示されますが、受信者の作成に使用されないカテゴリの行を含む、テンプレートの種類によって一時テーブルを整理することも。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

