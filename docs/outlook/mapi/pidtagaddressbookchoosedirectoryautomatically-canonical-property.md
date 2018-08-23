---
title: PidTagAddressBookChooseDirectoryAutomatically 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b685fd0ebe4a2d0bfcfd8aab3015602b84932db7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564942"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>PidTagAddressBookChooseDirectoryAutomatically 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
最も適切なグローバル アドレス一覧 (GAL) を選択するか、現在のメールボックスの連絡先フォルダーには、Microsoft Outlook 2010 と Microsoft Outlook 2013 を使用できます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|識別子:  <br/> |0x3D1C000B  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、アドレス帳のオプション] ダイアログ ボックスで**自動的に選択**の設定に対応します。 このプロパティが IID_CAPONE_PROF のプロファイル セクション内に存在する、Outlook 2010 または Outlook 2013 に**true を指定**アドレス帳ダイアログ不要になった、 [SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドで指定されたコンテナーのデフォルトが、アドレス帳を選択する設定は、ダイアログ ボックスが表示されていたコンテキストに適したと見なされます。 ありますが低い経験ではサード パーティのアドレス帳プロバイダーに注意してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI �萔](mapi-constants.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

