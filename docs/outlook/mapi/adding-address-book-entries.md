---
title: アドレス帳エントリの追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421341"
---
# <a name="adding-address-book-entries"></a>アドレス帳エントリの追加

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージングユーザーまたは配布リストをコンテナーに追加するために、クライアントは[IAddrBook:: newentry](iaddrbook-newentry.md)またはプロバイダーから[imapisupport:: newentry](imapisupport-newentry.md)を呼び出します。 _lpeidcontainer_パラメーターには、ターゲットコンテナーのエントリ id を指定します。 次に、MAPI は、1回限りのテーブルから1回限りのテンプレートを使用してエントリを作成するために、コンテナーの[IABContainer:: createentry](iabcontainer-createentry.md)メソッドを呼び出します。 1回限りのテンプレートでは、クライアントは特定の種類の新しい受信者を作成できます。 ほとんどのフィールドは編集できます。 _lな tryid_パラメーターで指定されているテンプレートは、プロバイダーが外部テンプレートをサポートしている場合に、プロバイダーが提供するか、外部プロバイダーからのテンプレートである可能性があります。 外部テンプレートから受信者を作成できるプロバイダーの**createentry**の実装は、常に、できないプロバイダーの実装よりも複雑です。 
  
 **IABContainer:: createentry を実装するには**
  
1. _lpentryid_パラメーターで指定されたエントリ id の種類を決定します。 
    
2. 入力識別子が、プロバイダーが所有するメッセージングユーザー、配布リスト、またはアドレス帳コンテナーのテンプレートを表している場合:
    
1. 適切なオブジェクトを作成し、初期化します。 プロバイダーは、必要に応じて、いくつかの初期プロパティを設定できます。 これらのプロパティは、作成される受信者の種類によって異なります。 
    
2. _lppMAPIPropEntry_パラメーターの内容で、オブジェクトの実装へのポインターを返します。 
    
3. エントリ識別子が外部プロバイダーのテンプレートを表す場合:
    
1. open [imapisupport:: openentry](imapisupport-openentry.md)を呼び出して、外部オブジェクトを開きます。 
    
2. プロパティタグ配列に NULL を渡すオブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、プロパティを取得します。 
    
3. 新しいオブジェクトに適用されず、転送されないすべてのプロパティのプロパティタグを PR_NULL に変更することによって、 **GetProps**から返されたプロパティ値の配列を編集します。 
    
4. 新しいオブジェクトのエントリ識別子を作成します。 
    
5. メッセージユーザーまたは配布リストのいずれかで、適切な種類の新しいオブジェクトを作成します。
    
6. 既定のプロパティを設定して、新しいオブジェクトを初期化します。
    
7. 外部オブジェクトが**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートしているかどうかを確認します。 
    
8. 外部オブジェクトが**PR_TEMPLATEID**をサポートしている場合は、 [imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)を呼び出して、外部プロバイダーから property オブジェクトインターフェイスを取得し、 _lppMAPIPropEntry_パラメーターの内容を foreign プロパティに設定します。オブジェクトの実装。 
    
9. 外部オブジェクトが**PR_TEMPLATEID**をサポートしていない場合は、 _lppMAPIPropEntry_パラメーターの内容をプロバイダーの新しいオブジェクトの実装に設定します。 
    
10. _lppMAPIPropEntry_パラメーターによって指定されるオブジェクトの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、外部オブジェクトから適切なプロパティを設定します。 
    

