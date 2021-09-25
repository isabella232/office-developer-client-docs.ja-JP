---
title: PidTagFormVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFormVersion
api_type:
- HeaderDef
ms.assetid: f2220060-65ea-4969-88d7-8348bd5aa242
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3f897248140b59dea20238c7d1eddf70b77c4aeb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587686"
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

