---
title: PidTagResolveMethod 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f55b85e21f007be7c1b9d42d42473e3a8d2becb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803361"
---
# <a name="pidtagresolvemethod-canonical-property"></a>PidTagResolveMethod 標準プロパティ

  
  
**適用対象**: Outlook 
  
フォルダーの競合の解像度の値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOLVE_METHOD  <br/> |
|識別子:  <br/> |0x3FE7  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>注釈

競合解決メッセージを含むフォルダーでこのプロパティは、競合を解決する方法を示します。 このプロパティが必要ではありません。 ただし、設定されている場合以外の次のフラグする必要がありますは使用されません。
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0X00000000)  <br/> |競合を解決すると、メッセージを生成する必要があります。  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0X00000001)  <br/> |現在の変更を適用する対象のメッセージを上書きします。  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0X00000002)  <br/> |パブリック フォルダー内のメッセージを解決する競合を生成するときに競合の通知メッセージを送信しません。  <br/> |
   
クライアントまたはサーバーする必要があります競合解決メッセージが関連付けられているメッセージを生成することができません。 **RESOLVE_METHOD_LAST_WRITER_WINS**セマンティクスを使用してこれらのメッセージを解決する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

