---
title: 既定のメッセージ ストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348602"
---
# <a name="opening-the-default-message-store"></a>既定のメッセージ ストアを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のセッションでは、1つのメッセージストアが既定のメッセージストアとして機能します。 既定のメッセージストアには、次のような特性があります。
  
- **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティは TRUE に設定されています。
    
- STATUS_DEFAULT_STORE フラグは、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティで設定されます。
    
- MAPI は、メッセージストアが開かれたときに、検索結果、共通ビュー、個人用ビューの IPM サブツリーとルートフォルダーを自動的に作成します。 これらのフォルダーの詳細については、「 [IPM Subtree](ipm-subtree.md) and [MAPI Special folders](mapi-special-folders.md)」を参照してください。 
    
既定のメッセージストアのエントリ識別子を取得するには、 [imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)を呼び出して、メッセージストアテーブルを開き、 [hrqueryallrows](hrqueryallrows.md)への呼び出しに適切な制限を適用する必要があります。 **hrqueryallrows**は、既定のメッセージストアを表す1行の行セットを返します。 **hrqueryallrows**に渡す制限は、次のいずれかの形式で行うことができます。 
  
1. **SAndRestriction**構造体を使用して結合する**と**、次のような制限があります。 
    
   - **PR_DEFAULT_STORE**プロパティが存在するかどうかをテストするために、 **sexistrestriction**構造を使用する存在する制限。 
    
   - **PR_DEFAULT_STORE**プロパティの TRUE 値をチェックするために[spropertyrestriction](spropertyrestriction.md)構造を使用するプロパティ制限。 
    
2. **PR_RESOURCE_FLAGS**プロパティに対するマスクとして STATUS_DEFAULT_STORE を適用するために[sbitmaskrestriction](sbitmaskrestriction.md)構造を使用するビットマスク制限。 
    
## <a name="see-also"></a>関連項目

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

