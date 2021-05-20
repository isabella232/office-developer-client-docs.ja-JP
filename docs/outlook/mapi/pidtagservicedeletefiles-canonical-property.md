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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436826"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>PidTagServiceDeleteFiles 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスのアンインストール時に削除するファイル名の一覧が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_DELETE_FILES、PR_SERVICE_DELETE_FILES_A、PR_SERVICE_DELETE_FILES_W  <br/> |
|識別子:  <br/> |0x3D10  <br/> |
|データの種類 :   <br/> |PT_MV_STRING8、PT_MV_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

コントロール パネルを使用してメッセージ サービスをアンインストールすると、これらのプロパティに含まれる一覧のファイル名がコンピューターから削除されます。 複数のメッセージ サービスをサポートする DLL や、追加のメッセージ サービスが誤って削除される可能性がある DLL をリストに含めずにしてください。
  
MAPI は、ANSI 文字セット内のファイル名と、そのファイルに渡される他の文字列でのみ動作します。 OEM 文字セットでファイル名を使用するアプリケーションは、MAPI を呼び出す前に ANSI に変換する必要があります。
  
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

