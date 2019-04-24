---
title: imapi進捗 getflags
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270268"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
進行状況の情報を計算する操作のレベルについて、progress オブジェクトからフラグ設定を返します。
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lアウトフラグ_
  
> 読み上げ進行状況情報を計算する操作のレベルを制御するフラグのビットマスク。 次のフラグを返すことができます。
    
MAPI_TOP_LEVEL 
  
> 処理を開始するためにクライアントによって呼び出されるオブジェクトの最上位レベルのオブジェクトの進行状況が計算されています。 たとえば、フォルダーコピー操作の最上位のオブジェクトは、コピーされているフォルダーです。 MAPI_TOP_LEVEL が設定されていない場合は、下位レベルのオブジェクトまたはサブオブジェクトの進行状況が計算されます。 フォルダーのコピー操作では、下位レベルのオブジェクトは、コピーされているフォルダー内のサブフォルダーの1つです。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フラグの値が正常に返されました。
    
## <a name="remarks"></a>解説

MAPI を使用すると、MAPI_TOP_LEVEL フラグを使用して、処理に関与するすべてのオブジェクトが同じ[imapiprogress](imapiprogressiunknown.md)実装を使用して進行状況を示すことができるように、サービスプロバイダーがトップレベルのオブジェクトとサブオブジェクトを区別できるようになります。 これにより、インジケーター表示が単一の正方向にスムーズに進みます。 MAPI_TOP_LEVEL フラグが設定されているかどうかによって、サービスプロバイダーが以降の呼び出しで progress オブジェクトに対して他のパラメーターを設定する方法が決まります。 
  
**getflags**によって返される値は、最初は実装者によって設定され、その後、 [imapiprogress:: setlimits](imapiprogress-setlimits.md)メソッドを呼び出してサービスプロバイダーによって設定されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

常にフラグを MAPI_TOP_LEVEL に初期化してから、必要に応じてサービスプロバイダーにクリアするようにします。 サービスプロバイダーは、 **imapiprogress:: setlimits**メソッドを呼び出して、フラグをクリアおよびリセットできます。 **getflags**およびその他の**imapiprogress**メソッドを実装する方法の詳細については、「[進行状況インジケーターの実装](implementing-a-progress-indicator.md)」を参照してください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

進行状況インジケーターを表示する場合は、最初に**imapiprogress:: getflags**への呼び出しを呼び出します。 すべての実装は、 _lMAPI_TOP_LEVEL flags_パラメーターの内容をこの値に初期化するため、戻り値はである必要があります。 progress オブジェクトへの一連の呼び出しの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |cmapiprogress 進行状況:: getflags  <br/> |mfcmapi は、 **imapiprogress:: getflags**メソッドを使用して、どのフラグが設定されているかを判別します。 **imapiprogress:: setlimits**メソッドを使用してフラグが設定されていない限り、MAPI_TOP_LEVEL を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[コード サンプルとしての MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

