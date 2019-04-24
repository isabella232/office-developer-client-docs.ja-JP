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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360775"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>PidTagDisplayTypeEx 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
グローバルアドレス一覧のテーブルの行にエントリを表示する方法についての、エントリの種類を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|識別子:  <br/> |0x3905  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI アドレス帳  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、エントリの種類をグローバルアドレス一覧にどのように表示するかについて指定します。 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) では表現できない追加情報が提供されています。
  
> [!NOTE]
> **PR_DISPLAY_TYPE**およびこのプロパティの両方の値は、"DT_" で始まり、Mapitags で定義されます。 文書化されていないすべての値は MAPI 用に予約されています。 クライアントアプリケーションは、新しい値を定義せず、文書化されていない値を処理するために準備する必要があります。 
  
オブジェクトの属性をローカル、リモート、セキュリティ制御のいずれであるかを判断するのに役立つマクロがいくつかあります。 これらのマクロは次のとおりです。 
  
|**Macro**|**値**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID (v)  <br/> |(!!((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE (v)  <br/> |(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE (v)  <br/> |(((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL (v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |
   
これらのマクロの使用方法に関するいくつかの注意事項を次に示します。 
  
- エントリが別のフォレスト内のリモートエントリであるかどうかを確認するには、DTE_IS_REMOTE_VALID マクロをこのプロパティの値に適用して、DTE_FLAG_REMOTE_VALID フラグがエントリに設定されているかどうかを確認します。 リモートエントリの場合は、DTE_REMOTE マクロを使用してリモートエントリの種類を調べることができます。 
    
- **PR_DISPLAY_TYPE**の値が DT_DISTLIST で、かつ DTE_IS_REMOTE_VALID が false の場合は、単一フォレスト構成とフォレスト間の構成の両方で、このプロパティの値にマクロ DTE_LOCAL を適用すると、オブジェクトの種類をさらに詳しく識別できます。DT_DISTLIST (配布リスト) または DT_SEC_DISTLIST (セキュリティ配布リスト) のいずれかです。 
    
- マクロ DTE_LOCAL を**PR_DISPLAY_TYPE_EX**の値に適用し、DT_REMOTE_MAILUSER 型を返す場合、エントリはリモートエントリです。 
    
- 単一のフォレスト、またはレプリケーションがアクセス制御リスト (ACL) によって制御されているフォレスト間の構成では、DTE_IS_ACL_CAPABLE マクロを使用して、エントリがセキュリティプリンシパルであるかどうかを判断できます。
    
フォレスト間の構成では、 **PR_DISPLAY_TYPE**は DT_REMOTE_MAILUSER という値を持っています。 このプロパティの値にマクロ DTE_REMOTE を適用すると、リモートエントリの種類を取得することができるようになります。 リモートエントリには、次のような種類があります。 
  
|**リモートエントリの種類**|**値**|**説明**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0x00000003)  <br/> |動的配布リスト。  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |配布リスト  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |装置 (例: プリンターやプロジェクター)。  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |メールボックスを持つユーザー。  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |グローバルアドレス一覧のアドレス一覧のエントリ。  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |会議室。  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |セキュリティ配布リスト。  <br/> |
   
**PR_DISPLAY_TYPE**の値が DT_DISTLIST で、かつ DTE_IS_REMOTE_VALID が false の場合、単一フォレストとフォレスト間の構成の両方で、このプロパティの値に DTE_LOCAL マクロを適用すると、配布リストの種類を取得できるようになります。. 配布リストには、次の種類があります。 
  
|**配布リストの種類**|**値**|**説明**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |配布リスト  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |セキュリティ配布リスト。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
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

