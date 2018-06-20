---
title: Outlook ソーシャル コネクタ プロバイダーのエラー コード
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: プロバイダーは、次の表に示すエラー コードのいずれかを使用して、呼び出し側にエラーを返す必要があります。
ms.openlocfilehash: 9e9abfda5930926a873ac37d3372eff7100be8a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804457"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Outlook ソーシャル コネクタ プロバイダーのエラー コード

プロバイダーは、次の表に示すエラー コードのいずれかを使用して、呼び出し側にエラーを返す必要があります。 
  
|**Error**|**エラー コード (16 進数)**|**説明**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |ソーシャル ネットワーク サイトのネットワークで認証に失敗しました。  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |ソーシャル ネットワーク サイトへの接続には接続は有効ではありません。  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |一般障害エラーです。  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |無効な操作のために内部エラーが発生しました。  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |関数に無効な引数が渡されました。  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |前回の同期以降の変更は起こりません。  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |リソースが見つかりませんでした。  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |ソーシャル ネットワーク サイトへの要求は有効ですが、ソーシャル ネットワーク サイトでは実装されていません。  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |メモリ不足のエラーが発生しました。  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |OSC プロバイダーには、リソースのアクセス許可が拒否されました。  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |ソーシャル ネットワークのアカウントを構成するサーバーのバージョンはサポートされていません。  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |プロバイダーは、このバージョンの OSC プロバイダーの拡張機能をサポートしていません。  <br/> |
   
## <a name="remarks"></a>備考

結果のハンドル、または**HRESULT**と呼ばれる 32 ビットの数値を使用して、成功、警告、およびエラー値が返されます。 **HRESULT**は、何もへのハンドルではありません。値のエンコードされたいくつかのフィールドが含まれる 32 ビット値だけですることをお勧めします。 正の結果は、状態の成功を示す、ゼロの結果成功 (S_OK) の状態のないと負の結果は失敗を示します。 
  

