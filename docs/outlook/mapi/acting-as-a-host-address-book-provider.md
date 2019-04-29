---
title: ホストアドレス帳プロバイダーとして機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 202d4b4391de7553e39e50dc527df5502ebcefb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406466"
---
# <a name="acting-as-a-host-address-book-provider"></a>ホストアドレス帳プロバイダーとして機能

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ホストプロバイダーは、コンテナー内の他のプロバイダーからの受信者を含むアドレス帳プロバイダーで、その他のプロバイダーによって受信者の実装を部分的に管理することに依存します。 ホストプロバイダーは、これらの外部受信者のテンプレート識別子を使用して、これらの受信者のデータを外部プロバイダーのコードにバインドします。 このバインドプロセスは、プロバイダーが受信者の**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティを取得し、 [imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)の呼び出しに渡すと開始されます。 
  
プロバイダーが**imapisupport:: OpenTemplateID**を呼び出すと、MAPI はテンプレート識別子内の**MAPIUID**とプロバイダーによって登録された**MAPIUID**を照合し、プロバイダーの[IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)メソッドを呼び出します。 外部プロバイダーは、プロバイダーの property オブジェクトへのポインター、独自の property オブジェクトの実装、またはプロバイダーのオブジェクトをラップする実装に返すことができます。 返されるポインターは、 _lppMAPIPropNew_パラメーターの内容に配置されます。 
  
プロバイダーは、FILL_ENTRY フラグセットを使用して**imapisupport:: OpenTemplateID**を呼び出すかどうかを選択できます。 受信者が作成されているとき、またはプロバイダーが受信者のプロパティを更新してから長い時間が経過したときに、このフラグを設定します。 FILL_ENTRY フラグの一般的な使用方法は、プロバイダー内の受信者を元のと同期された状態に保つことです。 この種類の同期スケジュールを実装すると、パフォーマンスが向上します。 
  
 **外部の受信者の同期を維持するには**
  
1. 定期的に更新するための適切な間隔を決定します。 
    
2. タイムスタンプ imapisupport への各呼び出し[:: OpenTemplateID](imapisupport-opentemplateid.md)。 
    
3. 前回の呼び出しからの経過時間に基づいて、完全な更新を実行する必要があるかどうかを評価します。 完全な更新が必要な場合は、FILL_ENTRY フラグを使用して**imapisupport:: OpenTemplateID**を呼び出します。 必要でない場合は、呼び出しにフラグを設定しないようにします。 
    
クライアントがコピーされた受信者のプロパティの1つに対して要求を行うと、プロバイダーは要求を処理するか、または外部プロバイダーから提供されたコードを使用するかを選択できます。 プロバイダーは、外部プロバイダーが、imapiprop [:: openproperty](imapiprop-openproperty.md)を除く**imapiprop**を呼び出すことができます。 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求する**openproperty**への呼び出しは、常にプロバイダーに転送されます。
  
 **テンプレート識別子コードにアクセスするには**
  
1. 受信者を開き、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティを取得します。 **PR_TEMPLATEID**を使用できないために**GetProps**が失敗した場合、外部プロバイダーは、この受信者のテンプレート識別子と関連コードをサポートしていません。 プロバイダーは、すべてのメンテナンスで受信者の実装を使用する必要があります。 
    
2. テンプレート識別子が**GetProps**から返された場合は、 **imapiprop:: OpenTemplateID**メソッドの呼び出しで、受信者の**imapiprop**実装へのポインターを渡します。 受信者のプロパティのほとんどまたはすべてを更新する必要がある場合、または更新されていない場合には、FILL_ENTRY フラグを設定します。 
    
3. **OpenTemplateID**が外部プロバイダーの**imapiprop**実装を返す場合は、この実装へのポインターをクライアントに返します。 
    
4. **OpenTemplateID**が実装を返さない場合は、通常、外部プロバイダーがプロファイルに含まれていないため、プロバイダーの**imapiprop**実装へのポインターをクライアントに返します。 クライアントは、いずれかのインターフェイスを使用して、オブジェクトのプロパティを操作できる必要があります。 
    

