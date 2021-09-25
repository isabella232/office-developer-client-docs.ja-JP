---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: 0d5ebfe46d34c8ba2381900d445f47bd5ea08215
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587861"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**適用対象**: Outlook 2013 | Outlook 2016 
  
自動ロック解除用に個人用フォルダー (.pst) ファイルを登録し、HrTrustedPSTOverrideHandlerCallback へのそれ以上の呼び出しを回避します。
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>パラメーター

_pmval_
  
> [in]登録するダイナミック リンク ライブラリ (DLL) のパスへのポインターを含む [SPropValue](spropvalue.md) 構造体。 構造には、次の特性があります。 
    
   - ulPropTag [のPROP_TAG](prop_tag.md)(PT_MV_UNICODE、PROP_ID_NULL)。
    
   - NULL 終端 Unicode 文字文字列の配列に設定される MVszW 値プロパティ。 詳細については [、「SWStringArray」を参照](swstringarray.md) してください。 
    
> [!NOTE]
> SPropValue は、PST の内部範囲の MAPI プロパティに格納されます。 このプロパティは、通常の MAPI アプリケーションにはアクセスできません。 
  
## <a name="return-value"></a>戻り値

S_OK 
  
> 関数呼び出しが成功しました。
    
## <a name="remarks"></a>注釈

永続登録は、PST を開くデスクトップ検索やデスクトップ検索Outlook Windowsパフォーマンスに悪影響を及ぼす可能性があります。 永続登録の使用法を使用または拡張する場合のパフォーマンス効果を考慮してください。
  
> [!IMPORTANT]
> このメソッドは Unicode でのみ実装されます。 さらに、配列内のパスにファイル名の拡張子が含.dll。 
  
## <a name="see-also"></a>関連項目

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

