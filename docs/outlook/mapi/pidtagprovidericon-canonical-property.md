---
title: PidTagProviderIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 92407d56bd095135ac1c6c292aa4b1da4755e93c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803215"
---
# <a name="pidtagprovidericon-canonical-property"></a>PidTagProviderIcon 標準プロパティ

  
  
**適用対象**: Outlook 
  
カスタム アイコンまたは MAPI プロバイダーのオンラインとオフラインの両方の状態で Microsoft Office Outlook のステータス バーに表示されるアイコンを指定する Unicode 文字列が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_ICON、PR_PROVIDER_ICON_W  <br/> |
|識別子:  <br/> |0x3417  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、オンラインの状態での MAPI プロバイダーを表すカスタム アイコンを含むリソース ファイルを指定し、必要に応じて、オフラインの状態でもう 1 つのカスタム アイコンです。 Outlook は、常に Unicode 表示形式でこれらのプロパティを要求します。 
  
次のプロパティの値がモジュール mymod32.dll から ID 1001 のアイコンを読み込むし、オンライン状態のアイコンを使用するように Outlook に指示するたとえば、: `mymod32.dll,#1001`。 オフライン状態のプロバイダーに固有のアイコンがないため、この例では、ステータス バーの Outlook の標準オフライン アイコンが使用されます。 
  
次のプロパティの値もオフライン状態に使用する同じモジュールの ID 1002 のアイコンをロードするモジュールの mymod32.dll から ID 1001 のアイコンを読み込むし、オンラインの状態のアイコンを使用する Outlook に指示します。 `mymod32.dll,#1001,#1002`。 ステータス バーに [Outlook] アイコンを使用しません。 
  
既定では、カスタム アイコンを指定しない場合、プロバイダーがオンライン状態とオフライン状態の Outlook の既定のアイコンで表されます。 プロバイダーでは、ステータス バーのアイコンの横に表示される表示名をオプションで指定できます。 詳細については、 **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)) を参照してください。
  
## <a name="related-resources"></a>関連リソース

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

