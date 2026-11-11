知情授权预问诊采集编排器
门诊护士在患者到院前收集结构化问答，按用途绑定授权并把风险信号送入人工队列，系统不得输出诊断或处方。

测试：python3 -m unittest discover -s tests/consent_intake -p 'test_*.py'
构建：python3 -m compileall -q intake_hub tests/consent_intake
验收：python3 -m intake_hub.gateway.command --fixture fixtures/demo.json --database /tmp/consent_intake-acceptance.sqlite3
