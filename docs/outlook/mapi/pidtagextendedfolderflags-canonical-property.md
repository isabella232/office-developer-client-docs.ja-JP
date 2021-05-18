---
title: PidTagExtendedFolderFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316353"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>PidTagExtendedFolderFlags 標準プロパティ
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーに関する拡張フラグが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|識別子:  <br/> |0x36DA  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI コンテナー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、フォルダーのエンコードされたサブプロパティを含むバイナリ ストリームです。 これは、一連の可変長サブアイテムとして書式設定されます。 サブアイテムの最初の 8 ビットは ID フィールドで、サブアイテムが表すフラグの種類を示します。 2 番目の 8 ビットは、続くデータのバイト数です。
  
指定できる ID 値は次のとおりです。
  
- Invalid
    
   この値を使用しない
    
- ExtendedFlags
    
   データは、次のように書式設定された 4 バイトの値です。
    
   |**ビット**|**説明**|
   |:-----|:-----|
   |0 ～ 1  <br/> |予約済み。  <br/> |
   |2  <br/> |アプリケーションでポリシーの説明を表示する場合は、0 に設定します。  <br/> |
   |3-5  <br/> |予約済み。  <br/> |
   |6-7  <br/> |フォルダー内のメッセージ数の表示を制御します。  <br/> 0 - 既定の設定を使用する  <br/> 1 - 未読メッセージの数を使用する  <br/> 3 - メッセージの総数を使用する  <br/> |
   |8-31  <br/> |予約済み。  <br/> |
   
予約済みアイテムは無視できますが、既存の値を保持する必要があります。
    
- SearchFolderID
    
   データ フィールドは 16 バイトのフィールドです。 アプリケーションが永続的な検索フォルダーを作成する場合は、フォルダーのこのフィールドを、検索フォルダー メッセージの **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)バイナリ プロパティと同じ値に設定する必要があります。
    
- ToDoFolderVersion
    
   データ フィールドは 4 バイトのフィールドです。 アプリケーションが to-do 検索フォルダーを作成する場合は、フォルダー上のこのフィールドの値を"0x000c0000" のリトルエンド整数値に設定する必要があります。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> 共有カテゴリ リストや作業時間など、クライアントおよびサーバー構成データの場所とプロパティを指定します。
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> 検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目

- [MAPI のプロパティ](mapi-properties.md)
- [MAPI 標準プロパティ](mapi-canonical-properties.md)
- [標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
- [MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

