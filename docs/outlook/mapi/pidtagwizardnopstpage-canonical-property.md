---
title: PidTagWizardNoPstPage の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b94e1f2d66f89d680cc738968342de0fbcee5cda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19803670"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>PidTagWizardNoPstPage の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このプロパティには、プロファイル ウィザードは、個人メッセージ ストア (PST) のページを非表示にする場合は TRUE が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|識別子:  <br/> |0x6700  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |Exchange の管理  <br/> |
   
## <a name="remarks"></a>Remarks

サービス プロバイダーは、 [LAUNCHWIZARDENTRY](launchwizardentry.md)関数のプロトタイプでは関数を呼び出すときにこのプロパティを設定できます。 このプロパティは、プロバイダーがユーザー ダイアログ ボックスの中に表示される PST のページをしないことをプロファイル ウィザードに指示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

