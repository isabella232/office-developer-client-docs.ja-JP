---
title: ホストのアドレス帳プロバイダーとして動作しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cf52062eacbd13b45087df9d8558bffd43ccd744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799634"
---
# <a name="acting-as-a-host-address-book-provider"></a>ホストのアドレス帳プロバイダーとして動作しています。

  
  
**適用されます**: Outlook 
  
ホスト プロバイダーとは、そのコンテナー内の他のプロバイダーからの受信者が含まれていて、受信者のメンテナンスを部分的に制御するその他のプロバイダーの実装に依存しているアドレス帳プロバイダーです。 ホスト プロバイダーでは、これらの受信者が外部のテンプレート識別子を使用して、外部プロバイダーのコードにこれらの受信者に対してデータをバインドします。 プロバイダーは、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティ、受信者を取得し、 [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)への呼び出しに渡されます場合は、バインディング プロセスが開始されます。 
  
**IMAPISupport::OpenTemplateID**、MAPI プロバイダー呼び出し内の**MAPIUID**に一致して、 **MAPIUID**を持つテンプレート id プロバイダーが登録されているプロバイダーの[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)メソッドを呼び出します。 外部のプロバイダーは、プロバイダーのプロパティ オブジェクト、プロパティ オブジェクトの実装を独自にポインターを返すことがありますか、プロバイダーのオブジェクトをラップする、実装します。 返されるポインターは、 _lppMAPIPropNew_パラメーターの内容に配置されます。 
  
プロバイダーは、FILL_ENTRY フラグを設定して**IMAPISupport::OpenTemplateID**をコールするかどうかを選択できます。 受信者を作成するとき、または長い時間が経過、プロバイダーが、受信者のプロパティを更新するときは、このフラグを設定します。 FILL_ENTRY フラグの一般的な用途では、同期元プロバイダーで、受信者を保持します。 同期スケジュールのこの型を実装すると、パフォーマンスが向上します。 
  
 **外部の受信者を保持するのには次のように同期します。**
  
1. 定期的な更新プログラムの適切な間隔を決定します。 
    
2. 各タイムスタンプは、 [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)を呼び出します。 
    
3. 前回の呼び出し後に期限が切れている時間の量に基づくフル更新を実行する必要があるかどうかを評価します。 フル更新が必要な場合は、FILL_ENTRY フラグを使用して**IMAPISupport::OpenTemplateID**を呼び出します。 そうでないために必要な場合、呼び出しのフラグは設定しません。 
    
クライアント コピーの受信者のプロパティのいずれかを要求すると、プロバイダーはその要求を処理または外部のプロバイダーから提供されたコードを使用するかどうかを選択できます。 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)以外の**IMAPIProp**を呼び出し、されていない場合、プロバイダーは、ほとんどをインターセプトするための外部プロバイダーを期待できます。 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを要求する**OpenProperty**への呼び出しは常に、プロバイダーに転送されます。
  
 **テンプレート識別子のコードへのアクセス**
  
1. 受信者を開き、メソッドを呼び出して、 [IMAPIProp::GetProps](imapiprop-getprops.md) **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティを取得します。 **GetProps**には、 **PR_TEMPLATEID**が使用できないため失敗した場合、外部のプロバイダー サポートしていません、テンプレート識別子と関連するコードをこの受信者の。 プロバイダーは、すべてのメンテナンスのため、受信者の実装を使用する必要があります。 
    
2. **GetProps**からテンプレートの識別子が返された場合、受信者の**IMAPIProp**の実装では、 **IMAPISupport::OpenTemplateID**メソッドの呼び出しにし、ポインターを渡します。 受信者のプロパティのほとんどまたはすべてをする必要がある場合、FILL_ENTRY フラグを設定の作成時またはかどうかは、更新されていない間に、ように更新します。 
    
3. **OpenTemplateID**では、外部プロバイダーの**IMAPIProp**の実装が返された場合は、[クライアントにこの実装へのポインターを返します。 
    
4. **OpenTemplateID**が返されない場合、実装、通常プロファイルでは、外部のプロバイダーがないためクライアントに返す**IMAPIProp**プロバイダーへのポインター。 クライアントがいずれかのインターフェイスを使用してオブジェクトのプロパティを操作することがあります。 
    

