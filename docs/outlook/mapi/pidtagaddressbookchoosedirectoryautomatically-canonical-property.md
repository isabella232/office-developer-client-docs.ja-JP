---
title: PidTagAddressBookChooseDirectoryAutomatically 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 578cdaeaba7ea88249d5f87f5b5ebca2ab28e51d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571249"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>PidTagAddressBookChooseDirectoryAutomatically 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在Microsoft Outlook 2010、Microsoft Outlook 2013最も適切なグローバル アドレス一覧 (GAL) または連絡先フォルダーを選択できます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|識別子:  <br/> |0x3D1C000B  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、[アドレス帳の **オプション] ダイアログの** [自動的に選択する] 設定に対応します。 このプロパティが IID_CAPONE_PROF プロファイル セクションに存在し **、true** に設定されている場合、アドレス帳ダイアログは [SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドで指定されたコンテナーに既定で設定されなくなりましたが、Outlook 2010 または Outlook 2013 がダイアログが表示されたコンテキストに適したアドレス帳を選択します。 これにより、サードパーティのアドレス帳プロバイダーのエクスペリエンスが低下する可能性があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[MAPI �萔](mapi-constants.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

