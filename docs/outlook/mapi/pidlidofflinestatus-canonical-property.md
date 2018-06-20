---
title: PidLidOfflineStatus の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 34f50766c2c45d85bbb0bd9e12d32c5dd87e3cac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802061"
---
# <a name="pidlidofflinestatus-canonical-property"></a>PidLidOfflineStatus の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
[MS LISTSWS] を実装するサーバー上のドキュメント ファイルの状態を決定します。
  
|||
|:-----|:-----|
|関連するプロパティ  <br/> |dispidOfflineStatus  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085B9  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

