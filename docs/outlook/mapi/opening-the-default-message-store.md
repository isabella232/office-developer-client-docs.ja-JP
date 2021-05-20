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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436028"
---
# <a name="opening-the-default-message-store"></a>既定のメッセージ ストアを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のセッションでは、1 つのメッセージ ストアが既定のメッセージ ストアとして機能します。 既定のメッセージ ストアには、次の特性があります。
  
- プロパティ **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティは TRUE に設定されます。
    
- このSTATUS_DEFAULT_STOREフラグは、プロパティ **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) PR_RESOURCE_FLAGSで設定されます。
    
- MAPI は、メッセージ ストアを開く際に、検索結果、一般的なビュー、個人用ビューの IPM サブツリーとルート フォルダーを自動的に作成します。 これらのフォルダーの詳細については [、「IPM Subtree」および「MAPI Special](ipm-subtree.md) [Folders」を参照してください](mapi-special-folders.md)。 
    
既定のメッセージ ストアのエントリ識別子を取得するには [、IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) を呼び出してメッセージ ストア テーブルを開き [、HrQueryAllRows](hrqueryallrows.md)の呼び出しで適切な制限を適用する必要があります。 **HrQueryAllRows は** 、既定のメッセージ ストアを表す 1 行の行セットを返します。 **HrQueryAllRows** に渡す制限は、次のいずれかの形式で実行できます。 
  
1. 次 **の組** み合わせに **SAndRestriction 構造を使用する** AND 制限。 
    
   - **SExistRestriction** 構造体を使用して、プロパティの存在をテストする **PR_DEFAULT_STOREがあります。** 
    
   - [SPropertyRestriction](spropertyrestriction.md)構造体を使用して、プロパティの TRUE 値を確認するプロパティ **PR_DEFAULT_STOREします。** 
    
2. [SBitMaskRestriction](sbitmaskrestriction.md)構造体を使用して、STATUS_DEFAULT_STORE プロパティに対してマスクとして適用するビットマスク **PR_RESOURCE_FLAGS** 制限。 
    
## <a name="see-also"></a>関連項目

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

