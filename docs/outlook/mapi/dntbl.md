---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '最終更新日: 2012 年 7 月 5 日'
ms.openlocfilehash: 1106df7e7d0926f9a7a4d4d1f0d1425f1bf11371
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556764"
---
# <a name="dntbl"></a>DNTBL
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストアの内容の完全同期の一部として、[テーブルの状態をダウンロード](download-table-state.md)中に、サーバーからフォルダーの内容をダウンロードするための情報です。
  
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
  
> [in] 動作を変更するフラグです 
    
  - DNT_OK
    
    - [in] ダウンロードに成功しました。 クライアントは、サーバーから情報をダウンロードした後、これを設定します。
    
_pstmReserved1_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pstmReserved2_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pstmReserved3_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pstmReserved4_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pxicc_
  
>  [out] 内容変更のダウンロードをサポートする、**IExchangeImportContentsChanges** の内容インターフェイスのポインターです。 **IExchangeImportContentsChanges** の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
    
_pxihc_
  
>  [out] 階層の増分変更のダウンロードをサポートする、**IExchangeImportHierarchyChanges** の階層インターフェイスのポインターです。 **IExchangeImportHierarchyChanges** の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
    
_pszName_
  
>  [out] フォルダーの名前です。 
    
_ftLastMod_
  
>  [out] フォルダーの最終変更時刻です。 
    
_ulRights_
  
>  [out] フォルダーの **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** プロパティの値です。 
    
_feid_
  
>  [out] フォルダーのエントリ ID です。 
    
_uintReserved_
  
>  [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_rgte_
  
> [out] 通常 (または表示) アイテムと関連する (または非表示) アイテムの変更です。  *rgte [0]* は通常アイテム、*rgte [1]* は関連するアイテムに使います。 増分変更の同期 (ICS) を使用してダウンロードしている間に Outlook がこのメンバーを設定します。 ICS の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
    
_lpsrReserved_
  
>  [in]/[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_boReserved_
  
>  [in] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pReserved1_
  
>  [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pReserved2_
  
>  [in] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)  
- [MAPI 定数](mapi-constants.md) 
- [DNTBLE](dntble.md)

