---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: 優先される文字の形式では、クライアントがアクセスできるオブジェクトを作成します。
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384193"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

優先される文字の形式では、クライアントがアクセスできるオブジェクトを作成します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |msmapi32.dll  <br/> |
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

_pvUnwrapped_
  
> [in]最初のラップが解除された Outlook オブジェクトです。 次のインタ フェースのいずれかを実装する必要があります。
    
   - [IMailUser: IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx)、 [IMAPIFolder: IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx)、 [IMessage: IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx)、 [IMsgStore: IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx)、 [IMSLogon: IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)、または[IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx)。
    
_ulUnwrappedFlags_
  
> [in]ラップの最初のオブジェクトの特性を示すフラグです。 次の値の 1 つ以上にする必要があります。
    
   - DDLWRAP_FLAG_ANSI-Unwrapped オブジェクトは、ANSI です。
    
   - DDLWRAP_FLAG_UNICODE-Unwrapped オブジェクトには、UNICODE です。
    
_ulWrappedFlags_
  
>  [in]優先文字形式のフラグ。 次の値の 1 つ以上にする必要があります。 
    
   - DDLWRAP_FLAG_ANSI-Wrapped オブジェクトは、ANSI として公開されます。
    
   - DDLWRAP_FLAG_UNICODE-Wrapped オブジェクトを UNICODE として公開されます。
    
_pIID_
  
>  [in]ラップが解除されたオブジェクトでサポートされているインターフェイスの識別子これが不明な場合は、NULL に設定します。 
    
_pulReserved_
  
>  [in]このパラメーターは使用されません。 NULL にする必要があります。 
    
_fCheckWrap_
  
>  [in]テキストを折り返すには、その形式の_pvUnwrapped_をチェックする必要がある場合、このパラメーターを**true**に設定します。オブジェクトをチェックすることがなく折り返す必要がある場合は、 **false**に設定します。 
    
_ppvWrapped_
  
>  [out]要求された文字の形式で、要求されたオブジェクトへのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

_FCheckWrap_を**true**に設定すると、ラップされたオブジェクトを渡すことは、ラップが解除されたオブジェクトになります。 、返されたオブジェクトをラップするかどうかに関係なくクライアントでは、返されるオブジェクトの参照を解放する必要が。 
  
Msmapi32.dll のこの関数のアドレスを検索するには、 **GetProcAddress**を使用して、プロシージャ名として**HrCreateNewWrappedObject@28**を指定します。 
  
## <a name="see-also"></a>関連項目

- [データの劣化層 API について](about-the-data-degradation-layer-api.md)
- [定数 (データの劣化層 API)](constants-data-degradation-layer-api.md)

