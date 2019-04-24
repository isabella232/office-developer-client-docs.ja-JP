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
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286461"
---
# <a name="pidtagprovidericon-canonical-property"></a>PidTagProviderIcon 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オンライン状態とオフライン状態の両方で、Microsoft Office Outlook ステータスバーの MAPI プロバイダーに対して表示されるカスタムアイコンまたはアイコンを指定する Unicode 文字列が格納されています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_ICON、PR_PROVIDER_ICON_W  <br/> |
|識別子:  <br/> |0x3417  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI メッセージストア  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、オンライン状態の MAPI プロバイダーを表すカスタムアイコンを含むリソースファイルを指定します。また、オプションでオフライン状態の別のカスタムアイコンを指定することもできます。 Outlook では、これらのプロパティは常に Unicode 表記で要求されます。 
  
たとえば、次のプロパティ値は、Outlook がモジュール mymod32 からアイコン ID 1001 を読み込んで、そのアイコンをオンライン状態`mymod32.dll,#1001`に使用するように指示します。 この場合、オフライン状態のプロバイダー固有のアイコンはないため、ステータスバーには標準の Outlook オフラインアイコンが使用されます。 
  
次のプロパティ値は、Outlook がモジュール mymod32 からアイコン id 1001 をロードして、そのアイコンをオンライン状態で使用するように指示します。また、この同じモジュールからアイコン id 1002 を読み込んで`mymod32.dll,#1001,#1002`オフライン状態に使用することもできます。 ステータスバーでは、Outlook アイコンは使用されません。 
  
既定では、カスタムアイコンが指定されていない場合、プロバイダーは、オンライン状態およびオフライン状態の Outlook の既定のアイコンで表されます。 プロバイダーは、必要に応じて、ステータスバーのアイコンの横に表示される表示名を指定できます。 詳細については、「 **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md))」を参照してください。
  
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

