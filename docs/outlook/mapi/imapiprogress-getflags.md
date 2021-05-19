---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423644"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
進行状況の情報を計算する操作レベルの進行状況オブジェクトからフラグ設定を返します。
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [out]進行状況情報を計算する操作のレベルを制御するフラグのビットマスク。 次のフラグを返します。
    
MAPI_TOP_LEVEL 
  
> 処理を開始するためにクライアントによって呼び出されるオブジェクトである、トップ レベル のオブジェクトの進行状況が計算されています。 たとえば、フォルダー コピー操作のトップ レベル のオブジェクトは、コピーするフォルダーです。 このMAPI_TOP_LEVEL設定されていない場合、下位レベルのオブジェクトまたはサブオブジェクトの進行状況が計算されます。 フォルダー コピー操作では、下位レベルのオブジェクトは、コピーするフォルダー内のサブフォルダーの 1 つになります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> flags 値が正常に返されました。
    
## <a name="remarks"></a>注釈

MAPI を使用すると、サービス プロバイダーは、MAPI_TOP_LEVEL フラグを使用してトップ レベル のオブジェクトとサブオブジェクトを区別し、操作に関係するすべてのオブジェクトが同じ [IMAPIProgress](imapiprogressiunknown.md) 実装を使用して進行状況を表示できます。 これにより、インジケーターの表示が 1 つの正の方向にスムーズに進みます。 MAPI_TOP_LEVEL フラグを設定するかどうかは、サービス プロバイダーが後続の progress オブジェクトへの呼び出しで他のパラメーターを設定する方法を決定します。 
  
**GetFlags** によって返される値は、最初は実装者によって設定され、その後 [、IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドへの呼び出しを通じてサービス プロバイダーによって設定されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

常にフラグを初期化してMAPI_TOP_LEVEL、必要に応じてクリアするためにサービス プロバイダーに依存します。 サービス プロバイダーは **、IMAPIProgress::SetLimits** メソッドを呼び出すことによってフラグをクリアおよびリセットできます。 **GetFlags** および他の **IMAPIProgress** メソッドを実装する方法の詳細については、「Progress Indicator の実装 [」を参照してください](implementing-a-progress-indicator.md)。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

進行状況インジケーターを表示するときに、最初に **IMAPIProgress::GetFlags** を呼び出します。 すべての実装が  _lpulFlags_ パラメーターの内容をこの値に初期化MAPI_TOP_LEVEL、返される値を使用する必要があります。 progress オブジェクトへの呼び出しのシーケンスの詳細については、「進捗インジケーターを表示 [する」を参照してください](how-to-display-a-progress-indicator.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI は **IMAPIProgress::GetFlags** メソッドを使用して、設定されているフラグを決定します。 **IMAPIProgress::SetLimits** メソッドを使用してフラグが設定されていないMAPI_TOP_LEVELを返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[コード サンプルとしての MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

