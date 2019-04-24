---
title: PidTagContainerFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357548"
---
# <a name="pidtagcontainerflags-canonical-property"></a>PidTagContainerFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳コンテナーの機能を説明するフラグのビットマスクを含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|識別子:  <br/> |0x3600  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>解説

ビットマスクには、次の1つ以上のフラグを設定できます。
  
AB_FIND_ON_OPEN 
  
> コンテナーの内容を表示する前に制限を要求するダイアログボックスを表示します。 
    
AB_MODIFIABLE 
  
> エントリをコンテナーに追加したり、コンテナーから削除したりできます。 このフラグは、コンテナー内のエントリを変更できるかどうかを示すものではありません。
    
AB_RECIPIENTS 
  
> コンテナーは受信者を保持できます。 このフラグは、受信者がコンテナーに実際に存在するかどうか、またはそれらを追加または削除できるかどうかを示すものではありません。 
    
AB_SUBCONTAINERS 
  
> コンテナーは子コンテナーを保持できます。 このフラグは、コンテナー内にサブコンテナーが実際に存在するかどうか、または、それらを追加または削除できるかどうかを示すものではありません。 [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)をサポートするには、コンテナーに AB_SUBCONTAINERS を設定する必要があります。 
    
AB_UNMODIFIABLE 
  
> コンテナーにエントリを追加または削除することはできません。 このフラグは、コンテナー内のエントリを変更できるかどうかを示すものではありません。 
    
AB_FIND_ON_OPEN フラグは、オンラインサービスで使用するコンテナー、またはサーバーへの接続速度が遅いコンテナーに対して強くお勧めします。 AB_FIND_ON_OPEN が設定されたコンテナーが開かれると、表示されるメッセージングユーザーを制限する [**検索**] ダイアログボックスがユーザーに表示されます。 一部の仕様では、メッセージングユーザーを制限することで、コンテンツの表示を飛躍的に向上させることができます。 
  
AB_MODIFIABLE または AB_UNMODIFIABLE フラグを設定する必要があります。 両方のフラグを設定することにより、変更できるかどうかをコンテナーが認識しないこと、たとえば、変更がユーザーのアクセス権に依存しているかどうかを示すことができます。 この場合、クライアントアプリケーションは、呼び出しを試行し、リターンコードを調べて、コンテナーの機能を判別する必要があります。 通常、クライアントは AB_MODIFIABLE を調べることによって開始されます。 設定されている場合、クライアントは、コンテナーを変更し、戻り値を確認する呼び出しを行います。 
  
AB_MODIFIABLE フラグは、コンテナーに追加できるエントリの種類を示していません。 このことを確認するには、クライアントは適切な[openproperty](imapiprop-openproperty.md)メソッドを使用してコンテナーの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを開く必要があります。 **PR_CREATE_TEMPLATES**を開くと、コンテナーの1回限りのテーブルが返され、コンテナーに作成できるエントリの種類が一覧表示されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
[[MS-CHAP]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> ネームサービスプロバイダインターフェイス (NSPI) サーバーとのクライアントの通信を処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

