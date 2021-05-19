---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339187"
---
# <a name="upmov"></a>UPMOV
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
移動されたアイテムをアップロードする情報。 この情報は、アップロードの削除状態とアップロード[テーブルの状態](upload-delete-status-state.md)[の間に使用されます](upload-table-state.md)。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a>メンバー

_ulFlags_
  
> [in]アップロード中の適切な動作を決定するフラグ。
    
  - UPV_ERROR
    
    - [in]サーバー フォルダーを開く際に問題が発生しました。
    
  - UPV_DIRTY
    
    - [in]アップロードの状態が変更されました。 これは、クライアントがローカル ストアの状態の変更を追跡するために使用します。
    
  - UPV_COMMIT
    
    - [in]アップロード状態のコミット。
    
_pReserved_
  
>  [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pstmReserved_
  
>  [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pszName_
  
>  [out]移動先フォルダーの名前。 
    
  > [!NOTE]
  > このメンバーは UNICODE をサポートしていない。 
  
_feid_
  
>  [out]移動先フォルダーのエントリ ID。 
    
_pfld_
  
>  [in]サーバー フォルダーへのポインター。 
    
_pxicc_
  
>  [in]増分変更同期 (ICS) を使用する場合のコンテンツ変更のアップロードをサポートする **IExchangeImportContentsChanges** コンテンツ インターフェイスへのポインター。 **IExchangeImportContentsChanges** および ICS の詳細については [、「ICS 評価基準」を参照してください](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)。
    
_dwReserved_
  
>  [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pupmovNext_
  
>  [out]次の移動コンテキスト。 
    
_cEntMov_
  
>  [in]ここに移動したアイテムの数。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [FEID](feid.md)

