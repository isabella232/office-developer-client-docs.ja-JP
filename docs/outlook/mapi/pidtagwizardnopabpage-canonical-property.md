---
title: PidTagWizardNoPabPage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cdb7dde4853188eb0621dc3c2f45c2dc713441d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570241"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>PidTagWizardNoPabPage 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
このプロパティには、プロファイル ウィザードでは、個人用アドレス帳 (PAB) のページを非表示にする場合は TRUE が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|識別子:  <br/> |0x6701  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |Exchange の管理  <br/> |
   
## <a name="remarks"></a>注釈

サービス プロバイダーは、 [LAUNCHWIZARDENTRY](launchwizardentry.md)関数のプロトタイプでは関数を呼び出すときにこのプロパティを設定できます。 このプロパティは、プロバイダーがユーザー ダイアログ ボックスの中に表示される個人用アドレス帳ページをしないことをプロファイル ウィザードに指示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

