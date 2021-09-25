---
title: クラスター セーフ関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 178076fecedbe2eb2a254dcd10932e4f4f4ae60d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601415"
---
# <a name="cluster-safe-functions"></a>クラスター セーフ関数

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel 2013 では、Excel が専用のクラスター コネクタ インタ フェースを介して、高パフォーマンスのコンピューティング クラスターに対するユーザー定義関数 (UDF) 呼び出しをオフロードできます。計算クラスターのベンダーによりクラスター コネクタが提供されています。UDF の作成者は、作成する UDF をクラスター セーフとして宣言できます。クラスター コネクタが存在する場合、Excel はこれらの UDF の呼び出しをオフロードするためにクラスター コネクタに送信します。
  
Excel �́A�Čv�Z���ɃN���X�^�[ �Z�[�t UDF ����o����ƁA���ݎ��s���� XLL ���A�N���X�^�[ �Z�[�t UDF�A����єC�ӂ̃p�����[�^�[��N���X�^�[ �R�l�N�^�ɓn���܂��B�R�l�N�^�� UDF �Ăяo��������[�g�Ŏ��s���A���ʂ� Excel �ɕԂ��܂��B�ˑ����Ȃ��v�Z�����s����A�N���X�^�[ �R�l�N�^�� UDF �̎��s���������ƌ��ʂ� Excel �ɓn���āA�ˑ�����v�Z�𑱍s���܂��B���̔񓯊�����̃��J�j�Y���́A�񓯊��̓����Ǘ�����̂� UDF �쐬�҂ł͂Ȃ��N���X�^�[ �R�l�N�^�ł���Ƃ����_������΁A�񓯊� UDF �ɂ���Ďg�p����郁�J�j�Y���Ɠ����ł��B�ʏ�A�N���X�^�[ �R�l�N�^�� XLL shim ��������� XLL ��ǂݍ��݁A�v�Z�N���X�^�[ �m�[�h��� UDF ����s���܂��B
  
�N���X�^�[ �Z�[�t�Ƃ��� UDF ��錾���邵���݂́A�}���` �X���b�h�̍Čv�Z�Ɋւ��� UDF ����S�Ƃ��Đ錾���邵���݂Ɏ��Ă��܂��B�������AUDF �͕K��������� Excel �Z�b�V�����̑��� UDF �Ɠ����R���s���[�^�[��Ŏ��s�����킯�ł͂Ȃ����߁A�N���X�^�[ �Z�[�t UDF ��L�q����ۂɂ́A���܂��܂ȍl�����������݂��܂��B
  
To register a UDF as cluster-safe, you must call the [xlfRegister (Form 1)](xlfregister-form-1.md) callback function through the **Excel12** or **Excel12v** interface. For more information about these interfaces, see the [Excel4/Excel12](excel4-excel12.md) and [Excel4v/Excel12v](excel4v-excel12v.md). Registering a UDF as cluster-safe through the **Excel4** or **Excel4v** interface is not supported. 
  
�N���X�^�[ �Z�[�t�Ƃ��Ċ֐���o�^����ꍇ�́A�֐����N���X�^�[ �Z�[�t�ȕ��@�œ��삷�邱�Ƃ�m�F����K�v������܂��B�N���X�^�[ �R�l�N�^�̌����ȓ���͎����ɂ���ĈقȂ�܂����AUDF �́A���U�R���s���[�^�[ �V�X�e����Ŏ��s���A�܂����̂悤�ȓ�������悤�ɐ݌v����K�v������܂��B
  
- UDF �̓������̏�ԂɈˑ����Ȃ��B���Ƃ��΁AUDF �͊����̃�������L���b�V���ȂǂɈˑ����Ă��Ă͂Ȃ�܂���B
    
- UDF �̓N���X�^�[ �R�l�N�^ �v���o�C�_�[�ŃT�|�[�g����Ă��Ȃ� Excel �R�[���o�b�N����s���Ȃ��B
    
�N���X�^�[ �Z�[�t UDF �ɂ́A�N���X�^�[ �Z�[�t�̓���̑��ɂ�A���̂悤�ȋZ�p�I�Ȑ���������܂��B
  
1. XLOPER ���� ('P' �^�A'R' �^) �͎g�p�ł��܂���B
    
2. �͈͎Q�Ƃ�T�|�[�g���� XLOPER12 ���� ('U' �^) �͎g�p�ł��܂���B
    
3. �}�N�� �V�[�g�̓����̊֐��ł����Ă͂Ȃ�܂��� ('#' �� '&amp;' ��g�ݍ��킹�邱�Ƃ͂ł��܂���)�B
    
���s���Ԃ��Z�� UDF �̏ꍇ�́A�I�t���[�h�̃I�[�o�[�w�b�h�� UDF�̎��s�ɂ����鎞�Ԃ���傫���Ȃ��āA���̃C���t���X�g���N�`����g�p���Ă�قƂ�ǃv���X�ɂȂ�Ȃ��\��������܂��B
  
> [!NOTE]
> [!����] �N���X�^�[ �Z�[�t UDF �͔񓯊� UDF �Ƃ��Đ錾�ł��܂���B 
  
UDF �́A[xlRunningOnCluster](xlrunningoncluster.md) �R�[���o�b�N�֐���Ăяo�����Ƃɂ���āA�N���X�^�[ �R�l�N�^��g�p���Ď��s����Ă��邩�ǂ����𔻕ʂł��܂��B 
  

