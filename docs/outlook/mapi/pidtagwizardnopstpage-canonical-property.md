---
title: PidTagWizardNoPstPage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bcf42991c31cfb7313ee1a668b5423db1defbe33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586867"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>PidTagWizardNoPstPage 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル ウィザードが個人用メッセージ ストア (PST) ページを非表示にしている場合、このプロパティには TRUE が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|識別子:  <br/> |0x6700  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Exchange管理  <br/> |
   
## <a name="remarks"></a>注釈

サービス プロバイダーは [、LAUNCHWIZARDENTRY](launchwizardentry.md) 関数プロトタイプに基づいて関数を呼び出す場合に、このプロパティを設定できます。 このプロパティは、プロバイダーがユーザー ダイアログの間に PST ページを表示したくないとプロファイル ウィザードに指示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

