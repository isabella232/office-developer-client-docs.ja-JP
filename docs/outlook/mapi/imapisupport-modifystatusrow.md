---
title: imapisupportmodifystatusrow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417162"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しい行を追加するか、または既存の行を変更して、状態テーブルを変更します。
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _cvalues_
  
> 順番新規または変更された状態テーブルの行に含まれるプロパティの数。 
    
 _lpcolumnvals_
  
> 順番新規または変更された状態テーブルの行に列として含まれるプロパティを示すプロパティ値の配列へのポインター。
    
 _ulFlags_
  
> 順番状態テーブルの行を定義する情報を処理する方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
STATUSROW_UPDATE 
  
> _lpcolumnvals_で参照されている配列に含まれるプロパティを、新しい行ではなく既存の状態テーブルの行で結合するように MAPI に指示します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 状態テーブルが正常に更新されました。
    
## <a name="remarks"></a>注釈

**imapisupport:: modifystatusrow**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。 サービスプロバイダーは、ログオン時に**modifystatusrow**を呼び出して、状態テーブルに行を追加します。また、その他の場合は、セッション中に行を更新します。 **modifystatusrow**は、状態テーブルを構築するために必要な情報を MAPI に提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**modifystatusrow**を呼び出して、既存の [状態] テーブル行のプロパティを変更する場合は、STATUSROW_UPDATE フラグを設定します。 これにより、変更された列だけが_lpcolumnvals_パラメーターに渡されることが MAPI に通知されます。 
  
クライアントは、状態の表の情報を使用して、状態オブジェクトにアクセスできます。 
  
[状態テーブル] 行に含める必要のある列の完全な一覧については、「 [status Tables](status-tables.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

