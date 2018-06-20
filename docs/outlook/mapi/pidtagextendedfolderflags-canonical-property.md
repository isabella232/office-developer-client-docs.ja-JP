---
title: PidTagExtendedFolderFlags の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4a4d3c940539c23be8ec212cb85e3dd4f3a04aab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802745"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>PidTagExtendedFolderFlags の標準的なプロパティ
 
**適用されます**: Outlook 
  
フォルダーの拡張のフラグが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|識別子:  <br/> |0x36DA  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI のコンテナー  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、エンコードされたサブ フォルダーのプロパティを含むバイナリ ストリームです。 それは一連の可変長サブ項目として書式設定されます。 サブ項目の最初の 8 ビットでは、[ID] フィールドは、サブ項目を表すフラグの種類を示します。 2 つ目の 8 ビットは、次のデータのバイト数です。
  
使用可能な ID の値は次のとおりです。
  
- 無効
    
   この値は使用しないで
    
- ExtendedFlags
    
   データは、4 バイトの値が設定されています。
    
   |**ビット**|**説明**|
   |:-----|:-----|
   |0 ～ 1  <br/> |予約済み。  <br/> |
   |2  <br/> |アプリケーション ポリシーの説明を表示する必要がある場合は 0 に設定します。  <br/> |
   |3-5  <br/> |予約済み。  <br/> |
   |6-7  <br/> |フォルダー内のメッセージ数の表示を制御します。  <br/> 0 - 既定の設定を使用します。  <br/> 1-未読メ ッ セージの数を使用します。  <br/> 3 - メッセージの合計数を使用します。  <br/> |
   |8-31  <br/> |予約済み。  <br/> |
   
予約済みの項目は無視できますが、既存の値を保持する必要があります。
    
- SearchFolderID
    
   データ フィールドは、16 バイトのフィールドです。 値は**PR_WB_SF_TAG**と同じフォルダーにこのフィールドを設定する必要がありますアプリケーションは、永続的な検索フォルダーを作成する場合 ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) 検索フォルダーのメッセージにバイナリのプロパティです。
    
- ToDoFolderVersion
    
   データ フィールドは、4 バイト フィールドです。 アプリケーションは、[to do] 検索フォルダーを作成するには、リトル エンディアンの整数値に"0x000c0000"のフォルダーにこのフィールドの値を設定する必要があります。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> 場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。
    
[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目

- [MAPI プロパティ](mapi-properties.md)
- [標準の MAPI プロパティ](mapi-canonical-properties.md)
- [MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
- [MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

