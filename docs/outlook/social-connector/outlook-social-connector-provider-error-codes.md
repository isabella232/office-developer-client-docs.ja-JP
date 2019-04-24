---
title: Outlook Social Connector プロバイダーのエラーコード
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: プロバイダーは、次の表に示すいずれかのエラーコードを使用して、発信者にエラーを返す必要があります。
ms.openlocfilehash: 22a6e8d4ebf87157eaee630cc47f9f363150e839
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359858"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Outlook Social Connector プロバイダーのエラーコード

プロバイダーは、次の表に示すいずれかのエラーコードを使用して、発信者にエラーを返す必要があります。 
  
|**Error**|**エラーコード (16 進)**|**説明**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |ソーシャルネットワークサイトのネットワークで認証に失敗しました。  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |ソーシャルネットワークサイトへの接続に使用できる接続がありません。  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |一般的なエラーです。  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |無効な操作によって、内部エラーが発生しました。  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |関数に無効な引数が渡されました。  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |前回の同期以降の変更は発生していません。  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |リソースが見つかりません。  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |ソーシャルネットワークサイトへの要求は有効ですが、ソーシャルネットワークサイトによって実装されていません。  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |メモリ不足エラーが発生しました。  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |.osc プロバイダーがリソースに対する権限を拒否しました。  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |ソーシャルネットワークアカウントを構成するサーバーのバージョンはサポートされていません。  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |プロバイダーは、このバージョンの .osc プロバイダー拡張機能をサポートしていません。  <br/> |
   
## <a name="remarks"></a>解説

成功、警告、およびエラー値は、result handle と呼ばれる32ビットの数値または**HRESULT**を使用して返されます。 **HRESULT**は、どのようなものにも対応していません。値でエンコードされた複数のフィールドを持つ32ビットの値にすぎません。 正の値は、状態が "成功" であることを示し、0を指定すると状態なし (S_OK) が返され、負の値を指定するとエラーが発生します。 
  

