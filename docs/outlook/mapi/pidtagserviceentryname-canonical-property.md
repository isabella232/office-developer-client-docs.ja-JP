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
  
メッセージ サービスの構成用のエントリ ポイント関数の名前を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|識別子:  <br/> |0x3D0B  <br/> |
|データの種類 :   <br/> |PT_STRING8  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ サービスの実装者は、メッセージ サービスエントリ ポイントを提供しますが、エントリ ポイントは必要ありません。 ただし、エントリ ポイントは、関連する構成プロパティが存在する場合にのみ指定する必要があります。 これらのプロパティが存在しない場合、MAPI はエントリ ポイントが指定されていないと見なします。
  
エントリ ポイント関数が表示されるダイナミック リンク ライブラリ (DLL) の名前は、PR_SERVICE_DLL_NAME **(** [PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) プロパティによって指定されます。
  
メッセージ サービス エントリ ポイントの詳細については、「Service Provider Entry Point Function の実装 [」を参照してください](implementing-a-service-provider-entry-point-function.md)。
  
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

