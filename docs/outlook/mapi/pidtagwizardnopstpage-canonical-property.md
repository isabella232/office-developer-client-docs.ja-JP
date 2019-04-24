---
title: PidTagWizardNoPstPage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e816af2ce60b4c06ae14f720cf7c36d58468d09d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350723"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>PidTagWizardNoPstPage 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルウィザードで個人用メッセージストア (PST) のページを非表示にする場合は、このプロパティには TRUE が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|識別子:  <br/> |0x6700  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Exchange 管理  <br/> |
   
## <a name="remarks"></a>解説

サービスプロバイダーは、 [launchwizardentry](launchwizardentry.md)関数プロトタイプに基づいて関数を呼び出すときに、このプロパティを設定できます。 このプロパティは、ユーザーダイアログの間、プロバイダーが PST ページを表示しないようにすることを、プロファイルウィザードに通知します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

