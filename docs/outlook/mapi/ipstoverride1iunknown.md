---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315499"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用フォルダー ファイル (PST) ストア プロバイダーが PSTDisableGrow ポリシーを上書きできます。
  
|||
|:-----|:-----|
|継承元:  <br/> |IUnknown  <br/> |
|実装元:  <br/> |PST ストア プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |個人用フォルダー (.pst) ファイルの登録の一覧を取得します。  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |HrTrustedPSTOverrideHandlerCallback へのそれ以上の呼び出しを回避し、自動ロック解除用に個人用フォルダー ファイルを登録します。  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |成長のために個人用フォルダー ファイルのロックを解除します。  <br/> |
   
## <a name="remarks"></a>注釈

PST オーバーライド ハンドラー インターフェイス識別子は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は [、MAPI 定数](mapi-constants.md) のトピックで見つけ、それらをコピーしてコードに追加できます。 Microsoft Windows ソフトウェア開発キット (SDK) ヘッダー ファイル guiddef.h で定義されている DEFINE_GUID マクロを使用して、グローバル一意識別子 (GUID) 記号名をその値に関連付ける。 
  
詳細については、「PST オーバーライド[ハンドラーを実装して、2007 年の PSTDisableGrow](https://support.microsoft.com/kb/956070)ポリシーをバイパスするOutlook参照してください。
  
## <a name="see-also"></a>関連項目



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

