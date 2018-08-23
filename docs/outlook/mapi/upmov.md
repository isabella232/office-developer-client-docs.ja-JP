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
ms.openlocfilehash: 0a8e318f9bb5e538473e1b60c650e8730f692e50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577990"
---
# <a name="upmov"></a>UPMOV
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
移動されたアイテムをアップロードする方法の詳細については。 [アップロード ステータスの状態を削除](upload-delete-status-state.md)し、[テーブルの状態をアップロード](upload-table-state.md)中には、この情報が使用されます。
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [in]アップロード中に適切な動作を決定するフラグを設定します。
    
  - UPV_ERROR
    
    - [in]サーバーのフォルダーを開くときに問題です。
    
  - UPV_DIRTY
    
    - [in]アップロードの状態が変更されました。 ローカル ストアの状態の変更を追跡するためにクライアントによって使用されます。
    
  - UPV_COMMIT
    
    - [in]アップロード状態をコミットします。
    
_保持_
  
>  [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pstmReserved_
  
>  [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pszName_
  
>  [out]コピー先のフォルダーの名前です。 
    
  > [!NOTE]
  > このメンバーは、UNICODE をサポートしていません。 
  
_feid_
  
>  [out]コピー先のフォルダーのエントリ ID です。 
    
_pfld_
  
>  [in]サーバー フォルダーへのポインター。 
    
_pxicc_
  
>  [in]増分変更の同期 (ICS) を使用する場合、コンテンツの変更のアップロードをサポートする**IExchangeImportContentsChanges**の内容のインターフェイスへのポインターです。 **IExchangeImportContentsChanges**と ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
    
_dwReserved_
  
>  [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pupmovNext_
  
>  [out]次にコンテキストを移動します。 
    
_cEntMov_
  
>  [in]項目の番号をここに移動します。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
- [MAPI �萔](mapi-constants.md)
- [FEID](feid.md)

