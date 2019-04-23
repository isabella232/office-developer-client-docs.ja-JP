---
title: PidTagProviderDllName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980460"
---
# <a name="pidtagproviderdllname-canonical-property"></a>PidTagProviderDllName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI サービスプロバイダーのダイナミックリンクライブラリ (DLL) のベースファイル名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_DLL_NAME、PR_PROVIDER_DLL_NAME_A、PR_PROVIDER_DLL_NAME_W  <br/> |
|識別子:  <br/> |0x300a  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>解説

MAPI は DLL ファイルの名前付け規則を使用します。 文字列32をベース DLL 名に追加して、32ビットプラットフォームで実行されているバージョンを識別します。 たとえば、MAPI という名前があるとします。DLL が指定されている場合、MAPI は MAPI32 という名前を作成します。dll は、対応する32ビットバージョンの dll を表します。
  
これらのプロパティは、基本名を指定する必要があります。 MAPI は、文字列32を必要に応じて追加します。 このプロパティの一部として文字列32を含めると、エラーになります。
  
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

