---
title: アドレス帳識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f312f07386b74a58e6da814191c8b67a667e9fbd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572131"
---
# <a name="address-book-identifiers"></a>アドレス帳識別子

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのアドレス帳プロバイダーは、PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを使用して、メッセージング ユーザーおよび配布リスト オブジェクトにエントリ識別子を割り当てる。 クライアント アプリケーションは、これらのエントリ識別子を使用して、割り当てられているオブジェクトを開いてアクセスします。
  
アドレス帳では、他の 3 種類の識別子を使用してオブジェクトを表します。
  
- 一時エントリ識別子
    
- 1 回のテンプレート エントリ識別子
    
- テンプレート識別子
    
さまざまなエントリ識別子と、名前が付けられた類似性のため、各型がどのように使用され、作成されるかについて混乱しがちです。 
  
1 回限りエントリ識別子は、1 回限りまたはカスタム受信者と呼ばれる受信者の種類を開いてアクセスするために使用されるエントリ識別子です。 1 回の受信者は、プロファイル内のアドレス帳プロバイダーに属していない受信者です。 1 回限りに割り当てられたエントリ識別子は、1 回限り受信者用に特別に予約された形式を使用します。 1 回のエントリ識別子はオブジェクトを開いてアクセスするために使用されるので、オブジェクトは PR_ENTRYID プロパティに格納されます。
  
1 回のエントリ識別子と 1 回のエントリ識別子が作成されます。
  
- クライアント アプリケーションのユーザーが、アドレス帳内のエントリを表していない受信者をメッセージの受信者リストに追加する場合。
    
- クライアント アプリケーションのユーザーが、アドレス帳内のエントリを表していない受信者を変更可能なアドレス帳コンテナーに追加する場合。
    
- トランスポート プロバイダーが、関連するアドレス帳プロバイダーで処理できないアドレスを含むメッセージを受信した場合。
    
- トランスポート プロバイダーがゲートウェイに属するアドレスを含むメッセージを受信した場合。
    
最初の 2 つの状況では、クライアントは **IAddrBook::CreateOneOff** を呼び出して、1 回のエントリ識別子を新しく作成された 1 回の受信者に関連付ける。 2 番目の 2 つの状況では、トランスポート プロバイダーは **IMAPISupport::CreateOneOff** を呼び出して、一時エントリ識別子を外部アドレスに関連付ける。 詳細については [、「IAddrBook::CreateOneOff」](iaddrbook-createoneoff.md) および [「IMAPISupport::CreateOneOff」を参照してください](imapisupport-createoneoff.md)。
  
1 回のテンプレート エントリ識別子は、1 回きりを作成するためのテンプレートを開いてアクセスするために使用される短期エントリ識別子です。 アドレス帳プロバイダーと MAPI の両方が、特定の種類の受信者を作成するために必要な情報を入力するテンプレートを提供します。 これらのテンプレートに関する情報 (エントリ識別子を含む) は、一時テーブルに公開されます。 MAPI が **IABLogon::GetOneOffTable** メソッドまたはアドレス帳コンテナーの **IMAPIProp::OpenProperty** メソッドを呼び出して **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを要求するか、プロバイダーが **IMAPISupport::GetOneOffTable** を呼び出す場合、1 回切り替えテーブルが表示されます。 詳細については [、「IABLogon::GetOneOffTable](iablogon-getoneofftable.md) [、IMAPIProp::OpenProperty、IMAPISupport::GetOneOffTable」](imapiprop-openproperty.md)を [参照してください](imapisupport-getoneofftable.md)。
  
新しい 1 回分を作成するために、ユーザーは 1 回のテーブルに一覧表示されているテンプレートのいずれかを選択します。 クライアントは、選択した行の PR_ENTRYID 列 (選択したテンプレートの一時テンプレートエントリ識別子) を _lpEIDNewEntryTpl_ パラメーターの **IAddrBook::NewEntry** に渡します。 詳細については [、「IAddrBook::NewEntry」を参照してください](iaddrbook-newentry.md)。 MAPI では、一時テンプレートエントリ識別子を使用してテンプレートを表示し、ユーザーが受信者の作成に必要な情報を入力できます。 
  
テンプレート識別子は、一部のアドレス帳プロバイダーが、PR_ENTRYID プロパティに保持されているエントリ識別子に加えて、受信者に割り当てるエントリ識別子です。 プロバイダーは、テンプレート識別子を格納 **PR_TEMPLATEID** 受信者のプロパティ [(PidTagTemplateid)](pidtagtemplateid-canonical-property.md)プロパティを設定します。 アドレス帳プロバイダーによっては、受信者のテンプレート識別子とエントリ識別子プロパティに同じ値を割り当てる場合があります。
  
テンプレート識別子は、アドレス帳プロバイダーと MAPI によってのみ使用され、ホスト プロバイダーと呼ばれる 1 つのプロバイダーの受信者データを、外部プロバイダーと呼ばれる別のプロバイダーの受信者のコードにバインドします。 ホスト プロバイダーは、受信者の記憶域を提供します。外部プロバイダーがロジックを提供します。 バインド プロセスを使用すると、ホスト プロバイダーは、外部プロバイダーのコードを使用して、格納する受信者のデータを更新できます。
  
ホスト プロバイダーは、受信者を変更する準備ができたら **、IMAPISupport::OpenTemplateID** メソッドへの呼び出しで PR_TEMPLATEID プロパティを渡してバインド プロセスを開始します。 MAPI は **、IABLogon::OpenTemplateID** メソッドへの呼び出しを通じて、テンプレート識別子を適切な外部プロバイダーに転送してプロセスを続行します。 詳細については [、「IMAPISupport::OpenTemplateID」](imapisupport-opentemplateid.md) および [「IABLogon::OpenTemplateID」を参照してください](iablogon-opentemplateid.md)。 外部プロバイダーは受信者の **IMAPIProp** 実装へのポインターを返します。このポインターは、ホスト プロバイダーが独自の実装の代用として使用できます。 
  

