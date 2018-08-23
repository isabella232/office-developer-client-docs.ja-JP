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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8964ba8c4341bec431bdbc1690d639b345df8b1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800634"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**適用対象**: Outlook 
  
返します。 操作の進行状況に関する情報は、計算対象のレベルに進行中のオブジェクトから設定にフラグを設定します。
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [out]進捗状況の情報を計算する操作のレベルを制御するフラグのビットマスクです。 次のフラグを返すことができます。
    
MAPI_TOP_LEVEL 
  
> 進行状況は、最上位レベルのオブジェクトでは、操作を開始するクライアントによって呼び出されるオブジェクトの中に計算されます。 たとえば、フォルダーのコピー操作で最上位レベルのオブジェクトは、コピーされているフォルダーです。 MAPI_TOP_LEVEL が設定されていない場合は、下位レベルのオブジェクトまたはサブオブジェクトの進行状況が計算されます。 フォルダーのコピー操作では下位レベルのオブジェクトがコピーされているフォルダー内のサブフォルダーのいずれかです。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フラグの値が正常に返されました。
    
## <a name="remarks"></a>注釈

MAPI 最上位のオブジェクトを区別するためにサービス プロバイダーを有効にし、MAPI_TOP_LEVEL フラグを使用してサブオブジェクト操作ですべてのオブジェクトが含まれるように実装を使用できます同じ[IMAPIProgress](imapiprogressiunknown.md)の進行状況を表示します。 インジケーターの表示をスムーズに進むと 1 つの正の方向に発生します。 MAPI_TOP_LEVEL フラグが設定されているかどうかは、サービス プロバイダーが実行中のオブジェクトへの以降の呼び出しで他のパラメーターを設定する方法を決定します。 
  
**GetFlags**によって返される値は実装によって、後で[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドを呼び出すことによってサービス ・ プロバイダーによって最初に設定します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

常に MAPI_TOP_LEVEL フラグの内容を初期化しをオフにするときは、適切なサービス プロバイダーに任せることです。 サービス プロバイダーでは、オフにでき、 **IMAPIProgress::SetLimits**メソッドを呼び出すことによって、フラグをリセットすることができます。 **GetFlags**およびその他の**IMAPIProgress**メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

進行状況のインジケーターを表示する場合は、最初の呼び出しは、 **IMAPIProgress::GetFlags**呼び出しを行います。 返された値は、すべての実装がこの値を_lpulFlags_パラメーターの内容を初期化するため、MAPI_TOP_LEVEL にすることがあります。 進行中のオブジェクトへの呼び出しのシーケンスの詳細については、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI では、 **IMAPIProgress::GetFlags**メソッドを使用して、どのフラグが設定を確認します。 **IMAPIProgress::SetLimits**メソッドを使用して、フラグが設定されていない限り、MAPI_TOP_LEVEL を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

