---
title: アドレス帳エントリの追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1a73a432511244726466e3717c58a085455baa18
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605217"
---
# <a name="adding-address-book-entries"></a>アドレス帳エントリの追加

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング ユーザーまたは配布リストをコンテナーに追加するには、クライアントが [IAddrBook::NewEntry](iaddrbook-newentry.md)を呼び出すか、プロバイダーが _lpEIDContainer_ パラメーターのターゲット コンテナーのエントリ識別子を使用して [IMAPISupport::NewEntry](imapisupport-newentry.md)を呼び出します。 MAPI は、コンテナーの [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドを呼び出して、1 回きりテーブルから 1 回のテンプレートを使用してエントリを作成します。 1 回限定のテンプレートを使用すると、クライアントは特定の種類の新しい受信者を作成できます。 ほとんどのフィールドは編集可能です。 _lpEntryID_ パラメーターが示すテンプレートは、プロバイダーが提供するテンプレートか、プロバイダーが外部テンプレートをサポートしている場合は、外部プロバイダーのテンプレートである可能性があります。 外部テンプレートから受信者を作成できるプロバイダーの **CreateEntry** の実装は、できないプロバイダーの実装よりも常に複雑です。 
  
 **IABContainer を実装するには::CreateEntry**
  
1. lpEntryID パラメーターで指定されたエントリ識別子  _の種類を決定_ します。 
    
2. エントリ識別子が、プロバイダーが所有するメッセージング ユーザー、配布リスト、またはアドレス帳コンテナーのテンプレートを表す場合:
    
1. 適切なオブジェクトを作成して初期化します。 プロバイダーは、必要に応じていくつかの初期プロパティを設定できます。 これらのプロパティは、作成する受信者の種類によって異なります。 
    
2. _lppMAPIPropEntry_ パラメーターの内容でオブジェクトの実装へのポインターを返します。 
    
3. エントリ識別子が外部プロバイダーのテンプレートを表す場合:
    
1. [IMAPISupport::OpenEntry を呼び出して](imapisupport-openentry.md)、外部オブジェクトを開きます。 
    
2. オブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し、プロパティ タグ配列に NULL を渡してプロパティを取得します。 
    
3. **GetProps** から返されるプロパティ値配列を編集するには、新しいオブジェクトに適用されないすべてのプロパティのプロパティ タグを PR_NULL に変更し、転送する必要があります。 
    
4. 新しいオブジェクトのエントリ識別子を作成します。 
    
5. メッセージング ユーザーまたは配布リストのいずれかの適切な種類の新しいオブジェクトを作成します。
    
6. 既定のプロパティを設定して、新しいオブジェクトを初期化します。
    
7. 外部オブジェクトがプロパティ ([PidTagTemplateid](pidtagtemplateid-canonical-property.md) **)** プロパティPR_TEMPLATEIDサポートするかどうかを確認します。 
    
8. 外部オブジェクトが **PR_TEMPLATEID** をサポートしている場合は [、IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) を呼び出して、外部プロバイダーからプロパティ オブジェクト インターフェイスを取得し  _、lppMAPIPropEntry_ パラメーターの内容を外部プロパティ オブジェクトの実装に設定します。 
    
9. 外部オブジェクトが **PR_TEMPLATEIDをサポート** していない場合は  _、lppMAPIPropEntry_ パラメーターの内容を、プロバイダーの新しいオブジェクトの実装に設定します。 
    
10. _lppMAPIPropEntry_ パラメーターが指すオブジェクトの [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出して、外部オブジェクトから適切なプロパティを設定します。 
    

