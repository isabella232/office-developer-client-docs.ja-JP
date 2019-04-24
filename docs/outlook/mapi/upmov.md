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
  
移動されたアイテムをアップロードするための情報。 この情報は、削除の状態を[アップロード](upload-delete-status-state.md)し、[テーブルの状態](upload-table-state.md)をアップロードするときに使用されます。
  
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
  
> 順番アップロード中の適切な動作を決定するフラグ。
    
  - UPV_ERROR
    
    - 順番サーバーフォルダーを開くときに問題が発生します。
    
  - UPV_DIRTY
    
    - 順番アップロード状態が変更されました。 これは、クライアントがローカルストアの状態の変更を追跡するために使用されます。
    
  - UPV_COMMIT
    
    - 順番アップロード状態をコミットします。
    
_保持され_
  
>  [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pstmReserved_
  
>  [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pszName_
  
>  読み上げ宛先フォルダーの名前。 
    
  > [!NOTE]
  > このメンバーは UNICODE をサポートしていません。 
  
_feid_
  
>  読み上げ宛先フォルダーのエントリ ID。 
    
_pfld_
  
>  順番サーバーフォルダーへのポインター。 
    
_pxicc_
  
>  順番増分変更の同期 (ICS) を使用した場合のコンテンツの変更のアップロードをサポートする、 **iexchangeimportcontents changes**コンテンツインターフェイスへのポインター。 **iexchangeimportの内容の変更**および ics の詳細については、「 [ics の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)」を参照してください。
    
_dwreserved_
  
>  [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pupmovNext_
  
>  読み上げ次の移動コンテキスト。 
    
_cEntMov_
  
>  順番ここで移動したアイテムの数。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [FEID](feid.md)

