---
title: PidTagServiceEntryName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432472"
---
# <a name="pidtagserviceentryname-canonical-property"></a>PidTagServiceEntryName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスを構成するためのエントリポイント関数の名前を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|識別子:  <br/> |0x3D0B  <br/> |
|データの種類 :   <br/> |PT_STRING8  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

メッセージサービスの実装者は、メッセージサービスのエントリポイントを指定することをお勧めしますが、エントリポイントは必須ではありません。 ただし、関連する構成プロパティが存在する場合にのみ、エントリポイントを指定する必要があります。 これらのプロパティが存在しない場合、MAPI はエントリポイントが提供されていないことを前提としています。
  
エントリポイント関数が表示されるダイナミックリンクライブラリ (DLL) は、 **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) プロパティによって名前が付けられます。
  
メッセージサービスのエントリポイントの詳細については、「[サービスプロバイダーエントリポイント関数の実装](implementing-a-service-provider-entry-point-function.md)」を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

