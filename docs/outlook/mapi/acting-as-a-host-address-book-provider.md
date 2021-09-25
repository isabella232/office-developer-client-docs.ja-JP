---
title: ホスト アドレス帳プロバイダーとして機能する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2e6bd9f2370b086ad3b53dd9db35116da374655e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567901"
---
# <a name="acting-as-a-host-address-book-provider"></a>ホスト アドレス帳プロバイダーとして機能する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ホスト プロバイダーは、コンテナー内の他のプロバイダーからの受信者を含むアドレス帳プロバイダーであり、他のプロバイダーによる受信者の実装に依存して、そのメンテナンスを部分的に制御します。 ホスト プロバイダーは、これらの外部受信者のテンプレート識別子を使用して、これらの受信者のデータを外部プロバイダーのコードにバインドします。 このバインド プロセスは、プロバイダーが受信者の **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティを取得し [、IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)の呼び出しで渡すときに開始されます。 
  
プロバイダーが **IMAPISupport::OpenTemplateID** を呼び出す場合、MAPI はテンプレート識別子内の **MAPIUID** とプロバイダーによって登録された **MAPIUID** と一致し、プロバイダーの [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) メソッドを呼び出します。 外部プロバイダーは、プロバイダーのプロパティ オブジェクトへのポインター、独自のプロパティ オブジェクトの実装、またはプロバイダーのオブジェクトをラップする実装へのポインターを返す場合があります。 返されるポインターは  _、lppMAPIPropNew パラメーターの内容に配置_ されます。 
  
プロバイダーは **、IMAPISupport::OpenTemplateID** を呼び出すかどうかを選択し、FILL_ENTRY設定します。 受信者が作成されている場合、またはプロバイダーが受信者のプロパティを更新してから長い時間が経過した場合に、このフラグを設定します。 FILL_ENTRYフラグの一般的な使用は、プロバイダー内の受信者を元の受信者と同期し続ける方法です。 この種類の同期スケジュールを実装すると、パフォーマンスが向上します。 
  
 **外部受信者の同期を維持するには**
  
1. 定期的な更新の適切な間隔を決定します。 
    
2. [IMAPISupport::OpenTemplateID への各呼び出しのタイムスタンプ](imapisupport-opentemplateid.md)。 
    
3. 前回の呼び出し以降に期限切れになった時間に基づいて、完全な更新を実行する必要があるかどうかを評価します。 完全な更新が必要な場合は **、IMAPISupport::OpenTemplateID** を呼び出し、FILL_ENTRYします。 必要ない場合は、呼び出しでフラグを設定しない。 
    
クライアントがコピーされた受信者のプロパティの 1 つを要求すると、プロバイダーは要求自体を処理するか、外部プロバイダーから提供されたコードを使用するかどうかを選択できます。 プロバイダーは [、IMAPIProp::OpenProperty](imapiprop-openproperty.md)以外の **IMAPIProp** への呼び出しが、すべてではないにしても、外部プロバイダーが大部分を傍受すると予想できます。 **OpenProperty** への呼び出 **し** で、PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求すると、常にプロバイダーに転送されます。
  
 **テンプレート識別子コードにアクセスするには**
  
1. 受信者を開き [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_TEMPLATEID **(** [PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティを取得します。 **GetProps が** 使用できないPR_TEMPLATEID失敗した場合、外部プロバイダーはこの受信者のテンプレート識別子と関連するコードをサポートしません。 プロバイダーは、すべてのメンテナンスに受信者の実装を使用する必要があります。 
    
2. テンプレート識別子が **GetProps** から返される場合は **、IMAPISupport::OpenTemplateID** メソッドの呼び出しで、テンプレート識別子と受信者の **IMAPIProp** 実装へのポインターを渡します。 受信者のFILL_ENTRYのプロパティのほとんどまたはすべてを更新する必要がある場合(作成時など)、またはしばらく更新されていない場合は、FILL_ENTRY フラグを設定します。 
    
3. **OpenTemplateID が** 外部プロバイダーの **IMAPIProp** 実装を返す場合は、この実装へのポインターをクライアントに返します。 
    
4. **OpenTemplateID が** 実装を返さない場合は、通常、外部プロバイダーがプロファイルに存在しないので、プロバイダーの **IMAPIProp** 実装へのポインターをクライアントに返します。 クライアントは、いずれかのインターフェイスを使用してオブジェクトのプロパティを使用できる必要があります。 
    

