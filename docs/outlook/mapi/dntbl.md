---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: 6096118d72dfc51fb60025a55f581ebf97b000a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799967"
---
# <a name="dntbl"></a>DNTBL
 
**適用されます**: Outlook 
  
ストアの内容の完全な同期の一部として、[テーブルの状態をダウンロード](download-table-state.md)、実行中にサーバーからフォルダーの内容をダウンロードするための情報です。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a>メンバー

_ulFlags_
  
> [in]フラグの動作を変更するのには 
    
  - DNT_OK
    
    - [in]ダウンロードが正常に完了しました。 クライアントは、サーバーから情報をダウンロードした後、これを設定します。
    
_pstmReserved1_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pstmReserved2_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pstmReserved3_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pstmReserved4_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pxicc_
  
>  [out]コンテンツの変更のダウンロードをサポートする**IExchangeImportContentsChanges**の内容のインターフェイスへのポインターです。 **IExchangeImportContentsChanges**の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
    
_pxihc_
  
>  [out]**IExchangeImportHierarchyChanges**階層のインターフェイスへのポインターをサポートする階層の増分変更をダウンロードします。 **IExchangeImportHierarchyChanges**の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
    
_pszName_
  
>  [out]フォルダーの名前です。 
    
_ftLastMod_
  
>  [out]フォルダーの最終更新時刻。 
    
_ulRights_
  
>  [out]フォルダーの**[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** プロパティの値です。 
    
_feid_
  
>  [out]フォルダーのエントリ ID です。 
    
_uintReserved_
  
>  [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_rgte_
  
> [out]通常 (または非表示) の変更と関連付けられている (非表示) の項目です。  *rgte [0]* は、通常の項目については、 *rgte [1]* 関連付けられているアイテムです。 Outlook では、増分変更の同期 (ICS) を使用する場合は、ダウンロード中にこのメンバーを設定します。 ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
    
_lpsrReserved_
  
>  [の] [out] このメンバーは、Outlook の内部使用に予約して、サポートされていません。 
    
_boReserved_
  
>  [in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pReserved1_
  
>  [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pReserved2_
  
>  [in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション状態マシンについて](about-the-replication-state-machine.md)  
- [MAPI �萔](mapi-constants.md) 
- [DNTBLE](dntble.md)

