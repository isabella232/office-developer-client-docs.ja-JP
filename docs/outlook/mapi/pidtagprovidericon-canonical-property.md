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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425639"
---
# <a name="pidtagprovidericon-canonical-property"></a>PidTagProviderIcon 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オンライン状態とオフライン状態の両方の Microsoft Office Outlook ステータス バーに MAPI プロバイダーに表示するカスタム アイコンまたはアイコンを指定する Unicode 文字列が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_ICON、PR_PROVIDER_ICON_W  <br/> |
|識別子:  <br/> |0x3417  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、オンライン状態の MAPI プロバイダーを表すカスタム アイコンを含むリソース ファイルを指定し、必要に応じてオフライン状態の別のカスタム アイコンを指定します。 Outlook常に Unicode 表記でこれらのプロパティを要求します。 
  
たとえば、次のプロパティ値は、Outlook にモジュール mymod32.dll からアイコン ID 1001 を読み込み、そのアイコンをオンライン状態に使用するように指示します `mymod32.dll,#1001` 。 オフライン状態のプロバイダー固有のアイコンは表示されませんので、この場合、標準のオフライン Outlookアイコンがステータス バーで使用されます。 
  
次のプロパティ値は、Outlook に対して、モジュール mymod32.dll からアイコン ID 1001 を読み込み、そのアイコンをオンライン状態に使用し、この同じモジュールからアイコン ID 1002 を読み込み、オフライン状態に使用するように指示します。 `mymod32.dll,#1001,#1002` ステータス Outlookアイコンは使用されません。 
  
既定では、カスタム アイコンが指定されていない場合、プロバイダーはオンライン状態とオフライン状態Outlook既定のアイコンで表されます。 プロバイダーは、必要に応じて、ステータス バーのアイコンの横に表示する表示名を指定できます。 詳細については、「PR_PROVIDER_DISPLAY_NAME_W **(** [PidTagProviderDisplayName)」を参照してください](pidtagproviderdisplayname-canonical-property.md)。
  
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

