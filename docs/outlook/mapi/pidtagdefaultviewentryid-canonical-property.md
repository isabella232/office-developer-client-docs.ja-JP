---
title: PidTagDefaultViewEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270015"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>PidTagDefaultViewEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの既定のビューのエントリ識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|識別子:  <br/> |0x3616  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI コンテナー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、初期ビューとして設定する必要があるフォルダー ビューのエントリ識別子です。 "Normal" ビューを初期ビューとして使用する場合は、プロパティを設定する必要があります。
  
クライアント アプリケーションは、フォルダーを開く時点でこのプロパティを取得し、パフォーマンスの大幅な向上を実現できます。 このプロパティは、関連付けられたコンテンツ テーブルを開いて制限を提出するのではなく、既定のビューを取得するショートカットとして使用できます。
  
[IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)メソッドのサービス プロバイダーの実装では、フォルダーをコピーするときにこのプロパティをコピーできます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

