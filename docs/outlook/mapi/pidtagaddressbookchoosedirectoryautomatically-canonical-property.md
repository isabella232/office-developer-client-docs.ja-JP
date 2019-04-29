---
title: PidTagAddressBookChooseDirectoryAutomatically 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409665"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>PidTagAddressBookChooseDirectoryAutomatically 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
microsoft outlook 2010 および microsoft outlook 2013 を有効にして、現在のメールボックスに対して最も適切なグローバルアドレス一覧 (GAL) または連絡先フォルダーを選択します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|識別子:  <br/> |0x3D1C000B  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、[アドレス帳のオプション] ダイアログボックスの **[自動**設定] に対応します。 IID_CAPONE_PROF プロファイルセクションにこのプロパティが存在し、 **true**に設定されている場合、アドレス帳ダイアログは[SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドによって指定されたコンテナーに既定ではなくなりますが、outlook 2010 または outlook 2013 のアドレス帳を選択します。ダイアログが表示されたコンテキストに対して適切であると見なされます。 これにより、サードパーティのアドレス帳プロバイダーの動作が低下する可能性があることに注意してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[MAPI �萔](mapi-constants.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

