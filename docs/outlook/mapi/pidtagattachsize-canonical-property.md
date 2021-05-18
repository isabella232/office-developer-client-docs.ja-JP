---
title: PidTagAttachSize 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361090"
---
# <a name="pidtagattachsize-canonical-property"></a>PidTagAttachSize 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルのすべてのプロパティのサイズの合計 (バイト単位) が含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_SIZE  <br/> |
|識別子:  <br/> |0x0E20  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

添付ファイルのサブオブジェクトは、PR_ATTACH_SIZE **勧めします** 。 PR_ATTACH_SIZE に含まれる **合計には****、PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティまたは PR_ATTACH_DATA_OBJ **(** [PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティのサイズが含まれます。 したがって **、通常PR_ATTACH_SIZE** は添付ファイルの内容よりも大きくなります。 
  
このプロパティを使用すると、モデムによるリモート転送を実行する前に添付ファイルのおおよそのサイズを確認し、添付ファイルをディスクに保存するときに進行状況インジケーターを表示できます。 これは、添付された OLE オブジェクトで特に便利です。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagMessageSize 標準プロパティ](pidtagmessagesize-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

