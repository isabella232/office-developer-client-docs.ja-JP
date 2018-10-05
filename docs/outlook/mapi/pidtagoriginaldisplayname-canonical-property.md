---
title: PidTagOriginalDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b7aef416beb9eee70aeff8cf20cb38ae8e7993f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387385"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a>PidTagOriginalDisplayName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用アドレス帳またはその他の書き込み可能なアドレス帳をアドレス帳からコピーされるエントリの元の表示名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_DISPLAY_NAME、PR_ORIGINAL_DISPLAY_NAME_A、PR_ORIGINAL_DISPLAY_NAME_W  <br/> |
|識別子:  <br/> |0x3A13  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティには、コピーしたエントリの元のソースに関する情報が含まれています。
  
Nonread レポートでは、これらのプロパティには、レポートを生成する元のメッセージの受信者の表示名のコピーが含まれています。 元の受信者、配布リストの一部である場合は、レポートの配布リストの表示名が保持されます。
  
クライアント アプリケーションは、比較するのに表示名の変更前のコピーを与えることで、改変やエントリの「なりすまし」を防ぐためにこれらのプロパティを使用することができます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagTransmittableDisplayName 標準プロパティ](pidtagtransmittabledisplayname-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

