---
title: 実装する高度な検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4430b52b470b89bd7d81922b98b121b3a455768f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800927"
---
# <a name="implementing-advanced-searching"></a>実装する高度な検索

  
  
**適用されます**: Outlook 
  
いくつかのアドレス帳コンテナーは、クライアントの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 以外のプロパティで検索できるようにする、高度な検索機能をサポートします。 高度な検索をサポートするために、プロバイダーは、他のコンテナーの**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティを通じてアクセスできる特別なコンテナーを実装しなければなりません。 **PR_SEARCH**を入力し、高度な検索条件を編集するために使用するダイアログ ボックスについて説明する表示のテーブルへのアクセスを提供するコンテナー オブジェクトが含まれています。 
  
 **サポートするには、高度な検索**
  
1. 検索条件の各プロパティを定義します。
    
2. コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッド内のコードのセクションでは、 **PR_SEARCH**プロパティを処理します。 
    
1. クライアントが**IMAPIContainer**インターフェイスを要求していることを確認してください。 不適切なインターフェイスが要求されている場合は、失敗し、MAPI_E_INTERFACE_NOT_SUPPORTED を返します。 
    
2. **IMAPIContainer**インターフェイスをサポートする新しい検索オブジェクトを作成します。 
    
3. この時点で、コールされます検索コンテナーの**IMAPIProp::OpenProperty**メソッドに、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを取得します。 プロバイダーは、 [BuildDisplayTable](builddisplaytable.md)コンテナーの高度な検索] ダイアログ ボックスについて説明するを呼び出すことによって通常の表示のテーブルを提供する必要があります。
    
4. MAPI では、ユーザーが適切な検索条件を入力できるように、[検索] ダイアログ ボックスを表示します。 ユーザーが終了すると、MAPI は、検索条件を格納するコンテナーの[IMAPIProp::SetProps](imapiprop-setprops.md)のメソッドを呼び出します。 
    
5. 検索コンテナーのコンテンツ テーブルを要求するための呼び出しを行われます。 内容をテーブルにすると、すべての条件に一致するコンテナー内のエントリにします。
    

