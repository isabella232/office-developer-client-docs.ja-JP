---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: クライアントが優先文字形式でアクセスできるオブジェクトを作成します。
ms.openlocfilehash: 7832b495e8d5e7ee1849782269f073fd4fa28392
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552088"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

クライアントが優先文字形式でアクセスできるオブジェクトを作成します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|呼び出し元:  <br/> |Client  <br/> |
|実装元:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a>パラメーター

_pvUnwrapped_
  
> [in]最初にラップされていないオブジェクトOutlookします。 次のいずれかのインターフェイスを実装する必要があります。
    
   - [IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [in]ラップされていない初期オブジェクトを特徴付けるフラグ。 次の値の 1 つ以上を指定する必要があります。
    
   - DDLWRAP_FLAG_ANSI- アンラップされたオブジェクトは ANSI です。
    
   - DDLWRAP_FLAG_UNICODE- アンラップされたオブジェクトは UNICODE です。
    
_ulWrappedFlags_
  
>  [in]優先文字形式のフラグ。 次の値の 1 つ以上を指定する必要があります。 
    
   - DDLWRAP_FLAG_ANSI- ラップされたオブジェクトは ANSI として公開されます。
    
   - DDLWRAP_FLAG_UNICODE- ラップされたオブジェクトは UNICODE として公開されます。
    
_pIID_
  
>  [in]ラップされていないオブジェクトでサポートされるインターフェイスの識別子。不明な場合は NULL に設定します。 
    
_pulReserved_
  
>  [in]このパラメーターは使用されません。 NULL である必要があります。 
    
_fCheckWrap_
  
>  [in]_pvUnwrapped_**をラップ** する前に形式をチェックする必要がある場合は、このパラメーターを true に設定します。オブジェクトをチェック **せずにラップ** する場合は false に設定します。 
    
_ppvWrapped_
  
>  [out]要求された文字形式でラップされた、要求されたオブジェクトへのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

_fCheckWrap_ が true に設定されたラップされたオブジェクトを渡す **場合、ラップ** されていないオブジェクトになります。 返されるオブジェクトがラップされるかどうかに関係なく、クライアントは返されたオブジェクトの参照を解放します。 
  
**GetProcAddress** を使用してこの関数のアドレスを検索する場合は **msmapi32.dllプロシージャHrCreateNewWrappedObject@28** として指定します。 
  
## <a name="see-also"></a>関連項目

- [データの劣化層 API について](about-the-data-degradation-layer-api.md)
- [定数 (データ低下層 API)](constants-data-degradation-layer-api.md)

