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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286489"
---
# <a name="pidtagproviderdllname-canonical-property"></a>PidTagProviderDllName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI サービス プロバイダーのダイナミック リンク ライブラリ (DLL) の基本ファイル名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_DLL_NAME、PR_PROVIDER_DLL_NAME_A、PR_PROVIDER_DLL_NAME_W  <br/> |
|識別子:  <br/> |0x300A  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

MAPI では、DLL ファイルの名前付け規則を使用します。 文字列 32 を基本 DLL 名に追加して、32 ビット プラットフォームで実行されるバージョンを識別します。 たとえば、名前を指定MAPI.DLL MAPI は、対応する 32 ビット バージョンの DLL を表す名前 MAPI32.DLL を作成します。
  
これらのプロパティには、基本名を指定する必要があります。 MAPI は、必要に応じて文字列 32 を追加します。 このプロパティの一部として文字列 32 を含めた場合、エラーが発生します。
  
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

