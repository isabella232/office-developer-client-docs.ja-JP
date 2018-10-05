---
title: PidTagDisplayTypeEx 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393244"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>PidTagDisplayTypeEx 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
グローバル アドレス一覧のエントリをテーブル内の行に表示する方法について、エントリの種類が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|識別子:  <br/> |0x3905  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI アドレス帳  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、グローバル アドレス一覧での表示の方法について、エントリの種類を指定します。 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) で表すことができないその他の情報を提供します。
  
> [!NOTE]
> **PR_DISPLAY_TYPE**とこのプロパティの両方の値は、「dt _」で始まるし、Mapitags.h で定義されています。 記載されていないすべての値は、MAPI 用に予約されています。 クライアント アプリケーションは、新しい値を定義する必要がないと、文書化されていない値で対処するために準備する必要があります。 
  
ローカル、リモート、またはセキュリティ制御などのオブジェクトの属性を判断するのに役立ついくつかのマクロがあります。 これらのマクロは次のとおりです。 
  
|**マクロ**|**値**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!!((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |(((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0X00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0X00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |
   
これらのマクロを使用する方法について、いくつかのノートを次に示します。 
  
- エントリは、別のフォレスト内のリモートのエントリであるかどうかを確認するには、エントリに DTE_FLAG_REMOTE_VALID フラグが設定されているかどうかを確認するには、このプロパティの値に DTE_IS_REMOTE_VALID マクロを適用します。 リモート エントリがある場合を調べることができますし、リモート エントリの種類 DTE_REMOTE マクロを使用しています。 
    
- 単一フォレストとフォレスト間の両方の構成では、 **PR_DISPLAY_TYPE**が DT_DISTLIST、および DTE_IS_REMOTE_VALID の値は、このプロパティの値にマクロ DTE_LOCAL を適用することができます、オブジェクトの種類を識別するためDT_DISTLIST (配布リスト) または DT_SEC_DISTLIST (セキュリティの配布リスト) のいずれかです。 
    
- マクロ DTE_LOCAL を**PR_DISPLAY_TYPE_EX**の値に適用すると、DT_REMOTE_MAILUSER の種類を取得して、エントリがリモートのエントリとします。 
    
- 単一フォレストまたはレプリケーションにアクセス制御リスト (ACL) では、制御されているフォレスト間の構成では、エントリがセキュリティ プリンシパルであるかどうかを確認するのには、DTE_IS_ACL_CAPABLE マクロを使用できます。
    
クロス フォレスト構成の場合、 **PR_DISPLAY_TYPE** DT_REMOTE_MAILUSER の値があります。 このプロパティの値にマクロ DTE_REMOTE を適用すると、リモートのエントリの種類を取得することができます。 リモート エントリの種類、次のとおりです。 
  
|**リモート エントリの種類**|**値**|**説明**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0X00000003)  <br/> |動的配布リストです。  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0X00000001)  <br/> |配布リストです。  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0X00000008)  <br/> |プリンターやプロジェクターなどの機器です。  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0X00000000)  <br/> |メールボックスを持つユーザーです。  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0X00000000)  <br/> |グローバル アドレス一覧にアドレス一覧エントリです。  <br/> |
|DT_ROOM  <br/> |((ULONG) 0X00000007)  <br/> |会議室です。  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |配布リストのセキュリティです。  <br/> |
   
構成の場合、 **PR_DISPLAY_TYPE**に DT_DISTLIST と DTE_IS_REMOTE_VALID の値が設定されているときは両方単一のフォレストとフォレスト間で、このプロパティの値に DTE_LOCAL マクロを適用することができます配布リストの種類を取得します。. 配布リストの種類、次のとおりです。 
  
|**配布リストの種類**|**値**|**説明**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0X00000001)  <br/> |配布リストです。  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |配布リストのセキュリティです。  <br/> |
   
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



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

