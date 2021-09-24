---
title: PidTagDisplayTypeEx 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a40e4c8a7a4380304e57998b8f54a209f463bf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550695"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>PidTagDisplayTypeEx 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
グローバル アドレス一覧のテーブル内の行にエントリを表示する方法に関して、エントリの種類を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|識別子:  <br/> |0x3905  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、グローバル アドレス一覧での表示方法に関して、エントリの種類を指定します。 この情報は、このプロパティ [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)**で** PR_DISPLAY_TYPE追加情報を提供します。
  
> [!NOTE]
> プロパティとこのプロパティ **のPR_DISPLAY_TYPE** は "DT_" で始まり、Mapitags.h で定義されます。 文書化されていないすべての値は、MAPI 用に予約されています。 クライアント アプリケーションは、新しい値を定義し、文書化されていない値を処理する準備をする必要があります。 
  
ローカル、リモート、セキュリティ制御など、オブジェクトの属性を特定するのに役立つマクロがあります。 これらのマクロには、次のものが含まれます。 
  
|**Macro**|**値**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!!((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |(((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |
   
これらのマクロの使い方に関する注意事項を次に示します。 
  
- エントリが別のフォレストのリモート エントリであるかどうかを確認するには、DTE_IS_REMOTE_VALID マクロをこのプロパティの値に適用して、DTE_FLAG_REMOTE_VALID フラグがエントリに設定されているかどうかを確認します。 リモート エントリの場合は、リモート エントリの種類を確認するには、次のマクロを使用DTE_REMOTEできます。 
    
- 単一フォレスト構成とフォレスト間構成の両方で **、PR_DISPLAY_TYPE** の値が DT_DISTLIST で、DTE_IS_REMOTE_VALID が false の場合、マクロ DTE_LOCAL をこのプロパティの値に適用すると、オブジェクトの種類をさらに DT_DISTLIST (配布リスト) または DT_SEC_DISTLIST (セキュリティ配布リスト) として識別できます。 
    
- マクロ を DTE_LOCAL の値に適用PR_DISPLAY_TYPE_EX型をDT_REMOTE_MAILUSERすると、エントリはリモート エントリになります。 
    
- 単一のフォレストまたはフォレスト間構成で、レプリケーションがアクセス制御リスト (ACL) によって制御されている場合は、DTE_IS_ACL_CAPABLE マクロを使用して、エントリがセキュリティ プリンシパルであるかどうかを判断できます。
    
フォレスト間構成では **、PR_DISPLAY_TYPEの** 値がDT_REMOTE_MAILUSER。 このプロパティのDTE_REMOTEを適用すると、リモート エントリの種類を取得できます。 リモート エントリの可能な種類は次のとおりです。 
  
|**リモート エントリの種類**|**値**|**説明**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0x00000003)  <br/> |動的配布リスト。  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |配布リスト。  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |プリンターやプロジェクターなどの機器。  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |メールボックスを持つユーザー。  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |グローバル アドレス一覧のアドレス一覧エントリ。  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |会議室。  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |セキュリティ配布リスト。  <br/> |
   
単一フォレストとフォレスト間構成の両方で **、PR_DISPLAY_TYPE** の値が DT_DISTLIST と DTE_IS_REMOTE_VALID が false の場合は、このプロパティの値に DTE_LOCAL マクロを適用すると、配布リストの種類を取得できます。 使用できる配布リストの種類は次のとおりです。 
  
|**配布リストの種類**|**値**|**説明**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |配布リスト。  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |セキュリティ配布リスト。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

