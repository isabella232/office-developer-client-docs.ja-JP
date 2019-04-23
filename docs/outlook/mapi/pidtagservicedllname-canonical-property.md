---
title: PidTagServiceDllName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980455"
---
# <a name="pidtagservicedllname-canonical-property"></a>PidTagServiceDllName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
構成のために呼び出すメッセージサービスプロバイダーエントリポイント関数を含む DLL のファイル名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_DLL_NAME、PR_SERVICE_DLL_NAME_A、PR_SERVICE_DLL_NAME_W  <br/> |
|識別子:  <br/> |0x3d0a  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>解説

エントリポイント関数名が**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) メソッドに表示される場合、エントリポイントが存在することを示します。
  
MAPI は DLL ファイルの名前付け規則を使用します。 文字列32をベース DLL 名に追加して、32ビットプラットフォームで実行されているバージョンを識別します。 たとえば、MAPI という名前があるとします。DLL が指定されている場合、MAPI は MAPI32 という名前を作成します。dll は、対応する32ビットバージョンの dll を表します。
  
これらのプロパティは、基本名を指定する必要があります。 MAPI は、文字列32を必要に応じて追加します。 これらのプロパティの一部として文字列32を含めると、エラーが発生します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagProviderDllName 標準プロパティ](pidtagproviderdllname-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

