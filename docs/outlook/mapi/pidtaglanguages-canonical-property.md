---
title: PidTagLanguages の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLanguages
api_type:
- HeaderDef
ms.assetid: 16d4e92d-d48e-4e06-9886-2d21f3d10640
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3870ca7aaf8c1b178155d385f88e130a46d3b787
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802928"
---
# <a name="pidtaglanguages-canonical-property"></a>PidTagLanguages の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ASCII メッセージで採用されている言語の一覧が入ります。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_LANGUAGES、PR_LANGUAGES_A、PR_LANGUAGES_W  <br/> |
|識別子:  <br/> |0x002F  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティには、コンマで区切られた 2 桁の国/地域コードのシーケンスが含まれています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
