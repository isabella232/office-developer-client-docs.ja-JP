---
title: 高度な検索の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0ba9958588c476ae330b0f4a413361e80d54667a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571970"
---
# <a name="implementing-advanced-searching"></a>高度な検索の実装

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
いくつかのアドレス帳コンテナーは、クライアントの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 以外のプロパティで検索できるようにする、高度な検索機能をサポートします。 高度な検索をサポートするために、プロバイダーは、他のコンテナーの**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティを通じてアクセスできる特別なコンテナーを実装しなければなりません。 **PR_SEARCH**を入力し、高度な検索条件を編集するために使用するダイアログ ボックスについて説明する表示のテーブルへのアクセスを提供するコンテナー オブジェクトが含まれています。 
  
 **サポートするには、高度な検索**
  
1. 検索条件の各プロパティを定義します。
    
2. コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッド内のコードのセクションでは、 **PR_SEARCH**プロパティを処理します。 
    
1. クライアントが**IMAPIContainer**インターフェイスを要求していることを確認してください。 不適切なインターフェイスが要求されている場合は、失敗し、MAPI_E_INTERFACE_NOT_SUPPORTED を返します。 
    
2. **IMAPIContainer**インターフェイスをサポートする新しい検索オブジェクトを作成します。 
    
3. この時点で、コールされます検索コンテナーの**IMAPIProp::OpenProperty**メソッドに、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを取得します。 プロバイダーは、 [BuildDisplayTable](builddisplaytable.md)コンテナーの高度な検索] ダイアログ ボックスについて説明するを呼び出すことによって通常の表示のテーブルを提供する必要があります。
    
4. MAPI では、ユーザーが適切な検索条件を入力できるように、[検索] ダイアログ ボックスを表示します。 ユーザーが終了すると、MAPI は、検索条件を格納するコンテナーの[IMAPIProp::SetProps](imapiprop-setprops.md)のメソッドを呼び出します。 
    
5. 検索コンテナーのコンテンツ テーブルを要求するための呼び出しを行われます。 内容をテーブルにすると、すべての条件に一致するコンテナー内のエントリにします。
    

