---
title: アドレス帳のエントリを追加します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: adbfbb73ac0f5f1e1cba547fa7a91393891fdb1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799628"
---
# <a name="adding-address-book-entries"></a>アドレス帳のエントリを追加します。

  
  
**適用されます**: Outlook 
  
コンテナー、 [IAddrBook::NewEntry](iaddrbook-newentry.md)のクライアントの呼び出し、またはプロバイダーに、メッセージングのユーザーまたは配布リストを追加するのには、 _lpEIDContainer_パラメーター内の移行先コンテナーのエントリの識別子を使用して[IMAPISupport::NewEntry](imapisupport-newentry.md)を呼び出します。 MAPI は、次に、一時テーブルから 1 回限りのテンプレートを使用してエントリを作成するコンテナーの[IABContainer::CreateEntry](iabcontainer-createentry.md)のメソッドを呼び出します。 1 回限りのテンプレートは、特定の種類の新しい受信者を作成するクライアントを使用します。 ほとんどのフィールドは、編集できます。 _LpEntryID_パラメーターで指定されたテンプレートでは、いずれかのプロバイダーを提供する可能性がありますか、プロバイダーが外部のテンプレートをサポートしている場合、外部プロバイダーからのテンプレートがあります。 **CreateEntry**の外部のテンプレートからの受信者を作成できるプロバイダーの実装は、常にすることはできませんプロバイダーの実装よりも複雑です。 
  
 **IABContainer::CreateEntry を実装するには**
  
1. _LpEntryID_パラメーターで指定されたエントリの識別子の種類を決定します。 
    
2. 場合はエントリの識別子では、メッセージングのユーザー、配布リスト、または、プロバイダーが所有する、アドレス帳コンテナーのテンプレートを表します。
    
1. 作成し、適切なオブジェクトを初期化します。 プロバイダーは、必要な場合、いくつかの初期プロパティを設定できます。 これらのプロパティは、作成される受信者の種類によって異なります。 
    
2. _LppMAPIPropEntry_パラメーターの内容でのオブジェクトの実装へのポインターを返します。 
    
3. 場合はエントリの識別子は、外部プロバイダーのテンプレートを表します。
    
1. 外部オブジェクトを開くには、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)を呼び出します。 
    
2. そのプロパティを取得するプロパティ タグ配列の NULL を渡すオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。 
    
3. プロパティ タグを変更するすべてのプロパティの新しいオブジェクトには適用されませんし、転送してはいけません PR_NULL、 **GetProps**から返されるプロパティ値の配列を編集します。 
    
4. 新しいオブジェクトのエントリ id を作成します。 
    
5. 適切なオブジェクトを新規作成、いずれかのメッセージのユーザーまたは配布リストを入力します。
    
6. 既定のプロパティを設定することによって新しいオブジェクトを初期化します。
    
7. 外部のオブジェクトが**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティをサポートしているかどうかを確認してください。 
    
8. 外部オブジェクトは、 **PR_TEMPLATEID**をサポートする場合は、外部プロバイダーからのプロパティのオブジェクトのインターフェイスを取得し、 _lppMAPIPropEntry_パラメーターの内容を外部のプロパティを設定する[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)を呼び出すオブジェクトの実装です。 
    
9. 外部オブジェクトが**PR_TEMPLATEID**をサポートしていない場合は、新しいオブジェクトのプロバイダーの実装に_lppMAPIPropEntry_パラメーターの内容を設定します。 
    
10. 外部オブジェクトから適切なプロパティを設定するのには_lppMAPIPropEntry_パラメーターが指すオブジェクトの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。 
    

