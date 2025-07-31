# JavaJAM State Transition Traces

Gray Paper Compatibility: 0.6.7

ASN.1 Schema
```
OpaqueHash ::= OCTET STRING (SIZE(32))
StateKey ::= OCTET STRING (SIZE(31))
ByteSequence ::= OCTET STRING

TestCase ::= SEQUENCE {
    pre_state    TestState,
    block        Block,
    post_state   TestState
}

TestState ::= SEQUENCE {
    state_root   OpaqueHash,
    keyvals      KeyVals
}

KeyVal ::= SEQUENCE {
    key   StateKey,
    val   ByteSequence
}

KeyVals ::= SEQUENCE OF KeyVal
```

All transition vectors are based on the [Tiny](https://docs.jamcha.in/basics/chain-spec/tiny) chain specifications.