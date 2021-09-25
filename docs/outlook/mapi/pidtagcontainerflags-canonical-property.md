---
title: PidTagContainerFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8816d3cbb4c34330cdc970f1d197aeda415f9ed2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600373"
---
# <a name="pidtagcontainerflags-canonical-property"></a>PidTagContainerFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳コンテナーの機能を説明するフラグのビットマスクが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|識別子:  <br/> |0x3600  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

ビットマスクには、次のフラグを 1 つ以上設定できます。
  
AB_FIND_ON_OPEN 
  
> コンテナーの内容を表示する前に、制限を要求するダイアログ ボックスを表示します。 
    
AB_MODIFIABLE 
  
> エントリはコンテナーに追加および削除できます。 このフラグは、コンテナー内のエントリを変更できるかどうかを示す値ではありません。
    
AB_RECIPIENTS 
  
> コンテナーは受信者を保持できます。 このフラグは、コンテナー内に受信者が実際に存在するかどうか、または受信者を追加または削除できるかどうかを示すのではありません。 
    
AB_SUBCONTAINERS 
  
> コンテナーは子コンテナーを保持できます。 このフラグは、どのサブコンテナーが実際にコンテナーに存在するか、追加または削除できるかどうかを示すのではありません。 AB_SUBCONTAINERS [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)をサポートするには、コンテナーに設定する必要があります。 
    
AB_UNMODIFIABLE 
  
> コンテナーにエントリを追加したり、コンテナーから削除したりすることはできません。 このフラグは、コンテナー内のエントリを変更できるかどうかを示す値ではありません。 
    
オンライン サービスAB_FIND_ON_OPENサーバーへの低速接続で使用されるコンテナーには、このフラグを使用することを強くお勧めします。 設定されているコンテナーを開AB_FIND_ON_OPEN、表示されるメッセージング ユーザーを制限する[検索] ダイアログ ボックスがユーザーに表示されます。 メッセージング ユーザーを制限する部分的な仕様でも、コンテンツの表示を大幅に高速化できます。 
  
AB_MODIFIABLEまたはAB_UNMODIFIABLEフラグを設定する必要があります。 両方のフラグを設定すると、変更がユーザーのアクセス権に依存する場合など、コンテナーが変更できるかどうかがわかりません。 この場合、クライアント アプリケーションは呼び出しを試み、戻りコードを調べてコンテナーの機能を判断する必要があります。 通常、クライアントは、クライアントの検証からAB_MODIFIABLE。 設定されている場合、クライアントはコンテナーの変更を試み、戻り値を確認する呼び出しを行います。 
  
このAB_MODIFIABLEは、コンテナーに追加できるエントリの種類を示す値ではありません。 これを確認するには、クライアントは適切な [OpenProperty](imapiprop-openproperty.md)メソッドを使用してコンテナーのプロパティ [(PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)**プロパティを開** PR_CREATE_TEMPLATESする必要があります。 この **PR_CREATE_TEMPLATES** すると、コンテナーの 1 回のテーブルが返され、コンテナーに作成できるエントリの種類が一覧に表示されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとのクライアントの通信を処理します。
    
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

