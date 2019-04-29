---
title: アドレス帳の識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 822d83c4b77d06c2e000b391c7e229985470ccd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421572"
---
# <a name="address-book-identifiers"></a>アドレス帳の識別子

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのアドレス帳プロバイダーは、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを使用して、メッセージングユーザーおよび配布リストオブジェクトにエントリ識別子を割り当てます。 クライアントアプリケーションは、これらのエントリ識別子を使用して、割り当てられているオブジェクトを開いてアクセスします。
  
アドレス帳は、次の3種類の識別子を使用してオブジェクトを表します。
  
- 一時エントリ識別子
    
- 1回限りのテンプレートエントリ識別子
    
- テンプレート識別子
    
さまざまなエントリ識別子と、それらに関連する類似性があるため、それぞれの種類がどのように使用され、作成されるかについて、簡単に混乱する可能性があります。 
  
1回限りのエントリ識別子は、1回限りの受信者またはカスタム受信者として知られる受信者の種類を開いてアクセスするために使用されるエントリ識別子です。 1回限りは、プロファイル内のどのアドレス帳プロバイダーにも属していない受信者です。 1回限りのエントリ識別子は、1回限りの受信者に対して明示的に予約された形式を使用します。 一時エントリ識別子は、オブジェクトを開いてアクセスするために使用されるため、PR_ENTRYID プロパティに格納されます。
  
1回限りの、または1回限りのエントリ識別子が作成されます。
  
- クライアントアプリケーションのユーザーが、アドレス帳のエントリを表さない受信者を、メッセージの受信者リストに追加することを選択した場合。
    
- クライアントアプリケーションのユーザーが、アドレス帳のエントリを表さない受信者を、変更可能なアドレス帳コンテナーに追加することを選択した場合。
    
- トランスポートプロバイダーは、関連するアドレス帳プロバイダーでは処理できないアドレスを持つメッセージを受信します。
    
- ゲートウェイに属するアドレスを持つメッセージをトランスポートプロバイダーが受信したとき。
    
最初の2つの状況で、クライアントは**IAddrBook:: createoneoff**を呼び出して、1回限りのエントリ識別子を新しく作成した受信者に関連付けます。 2番目の2つの状況では、トランスポートプロバイダーは**imapisupport:: createoneoff**を呼び出して、1回限りのエントリ識別子を外部アドレスに関連付けます。 詳細については、「 [IAddrBook:: createoneoff](iaddrbook-createoneoff.md) 」および「 [imapisupport:: createoneoff](imapisupport-createoneoff.md)」を参照してください。
  
1回限りのテンプレートエントリ識別子は、一時的なエントリ識別子です。これを使用して、1回の一時ファイルを作成するためのテンプレートを開いたり、テンプレートにアクセスしたりできます。 特定の種類の受信者を作成するために必要な情報を入力するためのアドレス帳プロバイダーと MAPI 提供テンプレートの両方。 これらのテンプレートに関する情報 (エントリ識別子を含む) は、1回限りのテーブルで公開されます。 MAPI が**IABLogon:: getoneofftable**メソッドまたはアドレス帳コンテナーの**imapiprop:: openproperty**メソッドを呼び出して、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) を要求すると、1回限りのテーブルが表示されます。プロパティ、またはプロバイダーが**imapisupport:: getoneofftable**を呼び出すとき。 詳細については、「 [IABLogon:: getoneofftable](iablogon-getoneofftable.md)」、「 [imapiprop:: openproperty](imapiprop-openproperty.md)」、および「 [imapi support:: getoneofftable](imapisupport-getoneofftable.md)」を参照してください。
  
新しい1回限りのテンプレートを作成するには、1回限りのテーブルにリストされているテンプレートの1つを選択します。 クライアントは、選択されている行から PR_ENTRYID 列を渡します。これは、選択したテンプレートの1回限りのテンプレートエントリ id であり、 _lpeidnewentrytpl_パラメーターの**IAddrBook:: newentry**になります。 詳細については、「 [IAddrBook:: newentry](iaddrbook-newentry.md)」を参照してください。 MAPI では、1回限りのテンプレートエントリ識別子を使用してテンプレートが表示され、ユーザーは受信者の作成に必要な情報を入力できるようになります。 
  
テンプレート識別子は、PR_ENTRYID プロパティに格納されているエントリ識別子に加えて、アドレス帳プロバイダーが受信者に割り当てるエントリ識別子です。 プロバイダーは、テンプレート識別子を格納するために受信者の**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティを設定します。 アドレス帳プロバイダーによっては、受信者のテンプレート識別子プロパティとエントリ id プロパティに同じ値が割り当てられます。
  
テンプレート識別子は、アドレス帳プロバイダーと MAPI によってのみ使用されます。ホストプロバイダーと呼ばれる1つのプロバイダーの受信者のデータを、別のプロバイダーの受信者のコードにバインドするには、外部プロバイダーと呼ばれます。 ホストプロバイダーは、受信者のストレージを提供します。外部プロバイダーがロジックを提供します。 バインドプロセスにより、ホストプロバイダーは、外部プロバイダーのコードを使用して格納される受信者のデータを更新できます。
  
ホストプロバイダーが受信者を変更する準備ができたら、PR_TEMPLATEID プロパティを**imapisupport:: OpenTemplateID**メソッドの呼び出しで渡して、バインドプロセスを開始します。 MAPI では、 **IABLogon:: OpenTemplateID**メソッドへの呼び出しによって、テンプレート識別子を適切な外部プロバイダーに転送することによって、プロセスを続行します。 詳細については、「 [imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md) and [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)」を参照してください。 外部プロバイダーは、受信者の**imapiprop**実装へのポインターを返します。これはホストプロバイダーが独自の実装の代わりに使用できます。 
  

