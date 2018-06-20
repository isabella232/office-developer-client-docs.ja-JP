---
title: PidTagStoreProvider の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b634f815d2aedecc716227c6525b846db38ca869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803593"
---
# <a name="pidtagstoreprovider-canonical-property"></a>PidTagStoreProvider の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ ・ ストアの種類を示すプロバイダー定義の[MAPIUID](mapiuid.md)構造体が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_MDB_PROVIDER  <br/> |
|識別子:  <br/> |0x3414  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>備考

[MAPIUID](mapiuid.md)構造体では、メッセージ ・ ストアの種類を識別します。 値は、メッセージ ストアのオブジェクトに、メッセージ ストア プロバイダーによって計算され、各プロバイダーに固有です。 パブリック フォルダーなど、目的の種類のストアを検索するのにはメッセージ ストアのテーブルを参照するために通常使用されます。 
  
このプロパティは、アドレス帳の**PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) のプロパティに似ています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

