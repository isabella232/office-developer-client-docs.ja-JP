---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: クライアントが適切な文字形式でアクセスできるオブジェクトを作成します。
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317606"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

クライアントが適切な文字形式でアクセスできるオブジェクトを作成します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|エクスポート対象:  <br/> |msmapi32  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
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

_pvunwrapped 解除_
  
> 順番最初にラップが解除された Outlook オブジェクト。 次のいずれかのインターフェイスを実装する必要があります。
    
   - [imailuser: imapiprop](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx)、 [imapiprop: IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx)、 [IMessage: imapiprop](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx)、 [IMsgStore: imapiprop](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx)、 [IMSLogon: IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)、または[iostx](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx)。
    
_ulUnwrappedFlags_
  
> 順番ラップされていない初期オブジェクトを特徴付けるフラグ。 次のいずれかの値であることが必要です。
    
   - DDLWRAP_FLAG_ANSI-ラップされていないオブジェクトは ANSI です。
    
   - DDLWRAP_FLAG_UNICODE-ラップされていないオブジェクトは UNICODE です。
    
_ulWrappedFlags_
  
>  順番優先する文字書式のフラグを指定します。 次のいずれかの値であることが必要です。 
    
   - DDLWRAP_FLAG_ANSI-ラップされたオブジェクトは、ANSI として公開されます。
    
   - DDLWRAP_FLAG_UNICODE-ラップされたオブジェクトは、UNICODE として公開されます。
    
_pIID_
  
>  順番ラップが解除されたオブジェクトによってサポートされるインターフェイスの識別子。この値が不明な場合は、NULL に設定します。 
    
_予約済み_
  
>  順番このパラメーターは使用されません。 NULL である必要があります。 
    
_fcheckwrap_
  
>  順番このパラメーターを**true**に設定すると、処理の前に_pvunwrapped ラップ_が解除されます。オブジェクトをチェックせずに折り返す必要がある場合は、 **false**に設定します。 
    
_ppvWrapped_
  
>  読み上げ要求された文字形式で囲まれた、要求されたオブジェクトへのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解説

_fcheckwrap_を**true**に設定してラップされたオブジェクトを渡すと、ラップが解除されたオブジェクトになります。 返されたオブジェクトがラップされているかどうかに関係なく、クライアントは返されたオブジェクトへの参照を解放する必要があります。 
  
**GetProcAddress**を使用して msmapi32 でこの関数のアドレスを検索する場合は、プロシージャ名として**HrCreateNewWrappedObject @ 28**を指定します。 
  
## <a name="see-also"></a>関連項目

- [データの劣化層 API について](about-the-data-degradation-layer-api.md)
- [定数 (データ低下層 API)](constants-data-degradation-layer-api.md)

