---
title: PidTagAddressBookChooseDirectoryAutomatically の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 48dfced07a8fd78a1af22679759effbd3c6da343
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802433"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>PidTagAddressBookChooseDirectoryAutomatically の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
最も適切なグローバル アドレス一覧 (GAL) を選択するか、現在のメールボックスの連絡先フォルダーには、Microsoft Outlook 2010 と Microsoft Outlook 2013 を使用できます。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|識別子:  <br/> |0x3D1C000B  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>備考

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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

