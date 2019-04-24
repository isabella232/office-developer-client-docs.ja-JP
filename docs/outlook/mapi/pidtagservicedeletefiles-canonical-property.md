---
title: PidTagServiceDeleteFiles 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336401"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>PidTagServiceDeleteFiles 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスがアンインストールされたときに削除されるファイル名の一覧が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_DELETE_FILES、PR_SERVICE_DELETE_FILES_A、PR_SERVICE_DELETE_FILES_W  <br/> |
|識別子:  <br/> |0x3d10  <br/> |
|データの種類 :   <br/> |PT_MV_STRING8、PT_MV_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティに含まれるリスト内のファイル名は、コントロールパネルを使用してメッセージサービスをアンインストールするときにコンピューターから削除されます。 複数のメッセージサービスをサポートする DLL がリストに含まれていない場合、または追加のメッセージサービスが誤って削除された可能性があります。
  
MAPI は、ファイル名、およびその他の文字列が ANSI 文字セットに渡された場合にのみ機能します。 OEM 文字セットでファイル名を使用するアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。
  
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

