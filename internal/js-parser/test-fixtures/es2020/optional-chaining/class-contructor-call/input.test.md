# `index.test.ts`

**DO NOT MODIFY**. This file has been autogenerated. Run `rome test internal/js-parser/index.test.ts --update-snapshots` to update.

## `es2020 > optional-chaining > class-contructor-call`

### `ast`

```javascript
JSRoot {
	comments: Array []
	corrupt: false
	directives: Array []
	filename: "es2020/optional-chaining/class-contructor-call/input.js"
	hasHoistedVars: false
	interpreter: undefined
	mtime: undefined
	sourceType: "script"
	syntax: Array []
	loc: Object {
		filename: "es2020/optional-chaining/class-contructor-call/input.js"
		end: Object {
			column: 12
			line: 1
		}
		start: Object {
			column: 0
			line: 1
		}
	}
	diagnostics: Array [
		Object {
			origins: Array [Object {category: "parse/js"}]
			location: Object {
				filename: "es2020/optional-chaining/class-contructor-call/input.js"
				mtime: undefined
				sourceText: undefined
				end: Object {
					column: 10
					line: 1
				}
				start: Object {
					column: 10
					line: 1
				}
			}
			description: Object {
				category: "parse/js"
				message: MARKUP {parts: Array [RAW_MARKUP {value: "constructors in/after an Optional Chain are not allowed"}]}
				advice: Array [
					log {
						category: "info"
						text: MARKUP {parts: Array [RAW_MARKUP {value: "Optional chain member responsible"}]}
					}
					frame {
						location: Object {
							filename: "es2020/optional-chaining/class-contructor-call/input.js"
							end: Object {
								column: 8
								line: 1
							}
							start: Object {
								column: 4
								line: 1
							}
						}
					}
				]
			}
		}
	]
	body: Array [
		JSExpressionStatement {
			loc: Object {
				filename: "es2020/optional-chaining/class-contructor-call/input.js"
				end: Object {
					column: 12
					line: 1
				}
				start: Object {
					column: 0
					line: 1
				}
			}
			expression: JSNewExpression {
				arguments: Array []
				optional: undefined
				typeArguments: undefined
				loc: Object {
					filename: "es2020/optional-chaining/class-contructor-call/input.js"
					end: Object {
						column: 12
						line: 1
					}
					start: Object {
						column: 0
						line: 1
					}
				}
				callee: JSMemberExpression {
					loc: Object {
						filename: "es2020/optional-chaining/class-contructor-call/input.js"
						end: Object {
							column: 10
							line: 1
						}
						start: Object {
							column: 4
							line: 1
						}
					}
					property: JSStaticMemberProperty {
						value: JSIdentifier {
							name: "d"
							loc: Object {
								filename: "es2020/optional-chaining/class-contructor-call/input.js"
								identifierName: "d"
								end: Object {
									column: 10
									line: 1
								}
								start: Object {
									column: 9
									line: 1
								}
							}
						}
						loc: Object {
							filename: "es2020/optional-chaining/class-contructor-call/input.js"
							identifierName: "d"
							end: Object {
								column: 10
								line: 1
							}
							start: Object {
								column: 9
								line: 1
							}
						}
					}
					object: JSMemberExpression {
						loc: Object {
							filename: "es2020/optional-chaining/class-contructor-call/input.js"
							end: Object {
								column: 8
								line: 1
							}
							start: Object {
								column: 4
								line: 1
							}
						}
						object: JSReferenceIdentifier {
							name: "C"
							loc: Object {
								filename: "es2020/optional-chaining/class-contructor-call/input.js"
								identifierName: "C"
								end: Object {
									column: 5
									line: 1
								}
								start: Object {
									column: 4
									line: 1
								}
							}
						}
						property: JSStaticMemberProperty {
							value: JSIdentifier {
								name: "b"
								loc: Object {
									filename: "es2020/optional-chaining/class-contructor-call/input.js"
									identifierName: "b"
									end: Object {
										column: 8
										line: 1
									}
									start: Object {
										column: 7
										line: 1
									}
								}
							}
							optional: true
							loc: Object {
								filename: "es2020/optional-chaining/class-contructor-call/input.js"
								identifierName: "b"
								end: Object {
									column: 8
									line: 1
								}
								start: Object {
									column: 7
									line: 1
								}
							}
						}
					}
				}
			}
		}
	]
}
```

### `diagnostics`

```

 es2020/optional-chaining/class-contructor-call/input.js:1:10 parse/js ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ constructors in/after an Optional Chain are not allowed

  ℹ Optional chain member responsible

    new C?.b.d()
        ^^^^

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```
