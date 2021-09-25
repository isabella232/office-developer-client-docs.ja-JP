---
title: Handler プロパティ (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1ea6d8a4ba0bb4a2b9a5a61e8241e853408b6263
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594210"
---
# <a name="handler-property-rds"></a>Handler プロパティ (RDS)

**適用先**: Access 2013、Office 2013

[RDSServer.DataFactory](datafactory-object-rdsserver.md)の機能を拡張するサーバー側カスタマイズ プログラム (ハンドラー) の名前と、ハンドラーで使用されるパラメーターを示 *します*。

## <a name="syntax"></a>構文

*DataControl*.Handler = *String*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*String* |ハンドラー **の** 名前と、すべてのパラメーターをコンマで区切って含む String 値 (たとえば、"handlerName,parm1,parm2,...,parm *N*")。|

## <a name="remarks"></a>注釈

このプロパティは、カスタマイズをサポートしますが、この機能を使用するには、[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定する必要があります。

ハンドラーの名前とパラメーターは、コンマ (",") で区切ります。*String* 内にセミコロン (";") が含まれていると、予期できない結果が発生する場合があります。また、**IDataFactoryHandler** インターフェイスをサポートしているハンドラーであれば、独自に作成することもできます。

既定のハンドラー名は **MSDFMAP.Handler** であり、この既定パラメーターは **MSDFMAP.INI** という名のカスタマイズ ファイルです。このプロパティは、サーバー管理者が作成した別のカスタマイズ ファイルを呼び出すときに使います。

**Handler** プロパティを設定するのに代わる方法としては、"**Handler=**_handlerName,parm1,parm2,...;_" のように [ConnectionString](connectionstring-property-ado.md) プロパティにハンドラーとパラメーターを指定します。

