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
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331403"
---
# <a name="pidtagresolvemethod-canonical-property"></a>PidTagResolveMethod 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの競合の解決の値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOLVE_METHOD  <br/> |
|識別子:  <br/> |0x3fe7  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>解説

競合の解決方法を含むフォルダーでこのプロパティを指定すると、競合を解決する方法が示されます。 このプロパティは必須ではありません。 ただし、これが設定されている場合は、次のようなフラグは存在しない必要があります。
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0x00000000)  <br/> |競合解決メッセージを生成する必要があります。  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)  <br/> |ターゲットメッセージを上書きして、現在の変更が適用されていることを示します。  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)  <br/> |パブリックフォルダーで競合の解決メッセージを生成するときに、競合の通知メッセージを送信しません。  <br/> |
   
クライアントまたはサーバーは、関連付けられたメッセージに対して競合の解決メッセージを生成してはなりません。 これらのメッセージは、 **RESOLVE_METHOD_LAST_WRITER_WINS**語義を使用して解決する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本データ構造を定義します。
    
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

