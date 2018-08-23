---
title: PidTagEmsAbServer 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 27e3a9687d66bd1cd3586a25a3ca5792523096c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802714"
---
# <a name="pidtagemsabserver-canonical-property"></a>PidTagEmsAbServer 標準プロパティ

  
  
**適用対象**: Outlook 
  
オフラインのシナリオ、またはオンラインのシナリオでは、アドレス帳コンテナーが存在するグローバル カタログ サーバーの完全修飾ドメイン名で、アドレス帳コンテナーのいずれかのパスを指定します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EMS_AB_SERVER、PR_EMS_AB_SERVER_A、PR_EMS_AB_SERVER_W  <br/> |
|識別子:  <br/> |0 xfffe  <br/> |
|データの種類 :   <br/> |PT_TSTRING  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、プロパティの型がコンパイル時に**PT_UNICODE**にリセット、`UNICODE`プラットフォームでは、Unicode、および**PT_STRING8**がコンパイルできないときに、シンボル、`UNICODE`の記号です。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義を提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

