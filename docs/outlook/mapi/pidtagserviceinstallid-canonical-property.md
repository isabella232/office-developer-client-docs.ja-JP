---
title: PidTagServiceInstallId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceInstallId
api_type:
- COM
ms.assetid: 1dd14858-2ce6-4629-a2f1-82d23cd6576b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 159a25347cd64b44f42dbb5052425ebb67894a9b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430372"
---
# <a name="pidtagserviceinstallid-canonical-property"></a>PidTagServiceInstallId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーのコンポーネント ID。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_INSTALL_ID、PR_SERVICE_INSTALL_ID_A、PR_SERVICE_INSTALL_ID_W  <br/> |
|識別子:  <br/> |0x3D13  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、プロバイダーをインストールする **MsiProvideQualifiedComponent** 呼び出しのコンポーネント パラメーターとして使用できます。 
  
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

