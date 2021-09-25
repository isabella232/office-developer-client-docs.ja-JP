---
title: PidTagServiceDllName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f01b9396e10d374ed2ddc152d3dadf3e8e5a3120
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604125"
---
# <a name="pidtagservicedllname-canonical-property"></a>PidTagServiceDllName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
構成を呼び出すメッセージ サービス プロバイダーエントリ ポイント関数を含む DLL のファイル名を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_DLL_NAME、PR_SERVICE_DLL_NAME_A、PR_SERVICE_DLL_NAME_W  <br/> |
|識別子:  <br/> |0x3D0A  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

エントリ ポイント関数名が PR_SERVICE_ENTRY_NAME **(** [PidTagServiceEntryName)](pidtagserviceentryname-canonical-property.md)メソッドに表示される場合、エントリ ポイントが存在することを示します。
  
MAPI では、DLL ファイルの名前付け規則を使用します。 文字列 32 を基本 DLL 名に追加して、32 ビット プラットフォームで実行されるバージョンを識別します。 たとえば、名前を指定MAPI.DLL MAPI は、対応する 32 ビット バージョンの DLL を表す名前 MAPI32.DLL を作成します。
  
これらのプロパティには、基本名を指定する必要があります。 MAPI は、必要に応じて文字列 32 を追加します。 これらのプロパティの一部として文字列 32 を含めた場合、エラーが発生します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagProviderDllName 標準プロパティ](pidtagproviderdllname-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

