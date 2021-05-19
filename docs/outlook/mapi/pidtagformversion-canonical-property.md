---
title: PidTagFormVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormVersion
api_type:
- HeaderDef
ms.assetid: f2220060-65ea-4969-88d7-8348bd5aa242
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ec806ed3ab871d6a36778b0898b2977628ccdcec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409868"
---
# <a name="pidtagformversion-canonical-property"></a>PidTagFormVersion 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのバージョンが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FORM_VERSION、PR_FORM_VERSION_A、PR_FORM_VERSION_W  <br/> |
|識別子:  <br/> |0x3301  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、フォームに対して現在有効なデザイン バージョンを示します。 バージョンはフォームのデザイナーによって定義および管理され、必ずしも MAPI コンポーネントのバージョンに関連する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

