---
title: 既定のメッセージ ストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1eb4e150be68ea01060c7afaed489c8759b576db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801671"
---
# <a name="opening-the-default-message-store"></a>既定のメッセージ ストアを開く

**適用されます**: Outlook 
  
特定のセッションでは、1 つのメッセージ ・ ストアは、既定のメッセージ ストアとして機能します。 既定のメッセージ ストアには、次の特徴があります。
  
- **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) のプロパティは、TRUE に設定されます。
    
- **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のプロパティで、STATUS_DEFAULT_STORE フラグが設定されています。
    
- メッセージ ストアを開いたときに、IPM サブツリーおよび検索の結果、一般的なビューと個人用ビューのルート フォルダー MAPI 自動的に作成します。 これらのフォルダーの詳細については、 [IPM サブツリー](ipm-subtree.md)および[MAPI の特別なフォルダー](mapi-special-folders.md)を参照してください。 
    
既定のメッセージ ストアのエントリ id を取得するには、メッセージ ストアのテーブルを開き、 [HrQueryAllRows](hrqueryallrows.md)への呼び出しで適切な制限を適用する[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出す必要があります。 **HrQueryAllRows**には、既定のメッセージ ストアを表す 1 つの行セットの行が返されます。 **HrQueryAllRows**に渡された制限は、形式は次のいずれかで実行できます。 
  
1. 結合する**SAndRestriction**構造体を使用して**** 制限します。 
    
   - **PR_DEFAULT_STORE**プロパティの存在をテストするのには**SExistRestriction**構造体を使用する制限が存在します。 
    
   - **PR_DEFAULT_STORE**プロパティに TRUE の値をチェックする[SPropertyRestriction](spropertyrestriction.md)構造体を使用するプロパティの制限。 
    
2. **PR_RESOURCE_FLAGS**プロパティをマスクとして STATUS_DEFAULT_STORE を適用するための[SBitMaskRestriction](sbitmaskrestriction.md)構造体を使用するビットマスクの制限。 
    
## <a name="see-also"></a>関連項目

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

