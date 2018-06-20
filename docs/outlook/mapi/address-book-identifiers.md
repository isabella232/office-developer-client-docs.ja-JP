---
title: アドレス帳の識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0814d76dac97e40940f41c49dbf72efdd26b3cca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799641"
---
# <a name="address-book-identifiers"></a>アドレス帳の識別子

  
  
**適用されます**: Outlook 
  
すべてのアドレス帳プロバイダーは、メッセージングのユーザーと配布リスト オブジェクトを**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを使用してエントリの識別子を割り当てます。 クライアント アプリケーションでは、これらのエントリの識別子を使用して、開き、それらが割り当てられているオブジェクトにアクセスします。
  
アドレス帳を使用して他の 3 つの種類の識別子オブジェクトを表します。
  
- 一時エントリ id
    
- エントリの識別子を 1 回限りのテンプレート
    
- テンプレート識別子
    
エントリの識別子は、その名前が類似の多様性は、各タイプの使用方法と作成方法がわからなくなりがちです。 
  
一時エントリの識別子を開くし、one-off と呼ばれる受信者やカスタム受信者の種類にアクセスするために使用するエントリの識別子です。 一時アドレスは、プロファイル内のアドレス帳プロバイダーのいずれかに属していない受信者です。 一時アドレスに割り当てられているエントリの識別子は、一時受信者の具体的には予約済みの形式を使用します。 一時エントリ id を開き、オブジェクトへのアクセスに使用するため、PR_ENTRYID プロパティに格納されます。
  
一時アドレスと 1 回限りのエントリの識別子が作成されます。
  
- クライアント アプリケーションのユーザーは、メッセージの受信者リストにアドレス帳のエントリを表していない受信者を追加できます。
    
- クライアント アプリケーションのユーザーは、変更可能なアドレス帳コンテナーに、アドレス帳のエントリを表していない受信者を追加できます。
    
- トランスポート プロバイダーは、関連するアドレス帳プロバイダーによっては処理できないアドレスを使用してメッセージを受け取ります。
    
- トランスポート プロバイダーは、ゲートウェイが所属するアドレスを使用してメッセージを受け取ります。
    
最初の 2 つの状況では、クライアントは、新しく作成された受信者が一時、一時エントリ id に関連付けるには、 **IAddrBook::CreateOneOff**を呼び出します。 2 つ目は 2 つの状況では、トランスポート プロバイダーは、外部アドレスを使用して 1 回限りのエントリの識別子を関連付けるには、 **IMAPISupport::CreateOneOff**を呼び出します。 詳細については、 [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)および[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)を参照してください。
  
1 回限りのテンプレートのエントリ id を開くし、一時アドレスを作成するためのテンプレートにアクセスするために使用する短期的なエントリ id です。 アドレス帳プロバイダーと MAPI の両方は、特定の種類の受信者を作成するために必要な情報を入力するためのテンプレートを指定します。 一時テーブルでは、それらのエントリの識別子を含む、これらのテンプレートについての情報が発行されます。 MAPI は、 **IABLogon::GetOneOffTable**メソッドまたは**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) を要求するためのアドレス帳コンテナーの**IMAPIProp::OpenProperty**メソッドを呼び出すと、一時テーブルが表示されます。プロパティまたはプロバイダーが**IMAPISupport::GetOneOffTable**を呼び出すとします。 詳細については、 [IABLogon::GetOneOffTable](iablogon-getoneofftable.md)、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)、および[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)を参照してください。
  
新しい one-off を作成するには、ユーザーは、1 回限りの表に記載されているテンプレートのいずれかを選択します。 クライアントは、 _lpEIDNewEntryTpl_パラメーターで**IAddrBook::NewEntry**を選択したテンプレートのテンプレートを 1 回限りのエントリ id には、選択した行から PR_ENTRYID 列を渡します。 詳細については、 [IAddrBook::NewEntry](iaddrbook-newentry.md)を参照してください。 MAPI は、テンプレートを表示して、受信者を作成するために必要な情報を入力するユーザーを許可するのには、1 回限りのテンプレートのエントリ id を使用します。 
  
テンプレート識別子は、いくつかのアドレス帳プロバイダーは、PR_ENTRYID プロパティを保持するエントリの識別子だけでなく、受信者に割り当てるエントリ識別子です。 プロバイダーでは、そのテンプレートの識別子を格納するのには受信者の**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティを設定します。 アドレス帳のプロバイダーによっては、受信者のテンプレートの識別子とエントリの識別子のプロパティに対して同じ値を割り当てます。
  
テンプレート識別子と MAPI アドレス帳プロバイダーによってのみ 1 つのプロバイダーに受信者のデータをバインドするために使用、別のプロバイダーに受信者のコードに、ホスト プロバイダーと呼ばれることは、外部のプロバイダーと呼ばれます。 ホスト プロバイダーは、受信者のストレージを提供します。外部のプロバイダーでは、ロジックを提供します。 バインド処理では、外部プロバイダーのコードを使用して格納する受信者のデータを更新するホスト プロバイダーを使用できます。
  
ホスト プロバイダーは、その受信者を変更する準備が、バインド処理を開始するには、 **IMAPISupport::OpenTemplateID**メソッドを呼び出すに PR_TEMPLATEID プロパティが渡されます。 MAPI では、テンプレートの識別子を**IABLogon::OpenTemplateID**メソッドを呼び出すことによって外部の適切なプロバイダーに転送するプロセスを続行します。 詳細については、 [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)および[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)を参照してください。 外部のプロバイダーは、ホスト プロバイダーが独自の実装の代わりに使用できる受信者の**IMAPIProp**実装へのポインターを返します。 
  

