---
title: PidLidOfflineStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7d9f8cf4fbdeab70e40447411ed8efd35ef7899e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588777"
---
# <a name="pidlidofflinestatus-canonical-property"></a>PidLidOfflineStatus 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[MS LISTSWS] を実装するサーバー上のドキュメント ファイルの状態を決定します。
  
|||
|:-----|:-----|
|関連するプロパティ  <br/> |dispidOfflineStatus  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085B9  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

次の表は、このプロパティの値を示しています。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |ドキュメントがチェック アウトされていません。  <br/> |
|1  <br/> |ドキュメントが現在のユーザーにチェック アウトします。  <br/> |
|2  <br/> |ドキュメントがチェック アウトされていません、ですが、現在のユーザーが現在のコンピューター上で編集するために保存するファイルのコピーを持っています。  <br/> |
   
このプロパティは、ローカルで計算されがサーバーに送信されません、いつでもユーザーが別のアカウントにアイテムをドラッグしない限り。 その場合は、ユーザー定義のカスタム プロパティとして扱われます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[MS OXPROPS] 
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

